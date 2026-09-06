# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | [optional] 
**username** | **str** | Handle the user can sign in with instead of their email. | [optional] 
**display_name** | **str** |  | [optional] 
**theme** | **str** | Which skin this person prefers, or null to take whatever their organization or the instance says. | [optional] 
**locale** | **str** | Which locale this person prefers, or null for no explicit choice — the same shape as {@see self::$theme}: null is not &#x60;en_GB&#x60;, it is \&quot;let the cascade decide\&quot; (cookie, then &#x60;Accept-Language&#x60;, then the instance default). See {@see \\App\\Service\\LocaleResolver} and docs/internationalization.md. | [optional] 
**timezone** | **str** | The IANA timezone identifier (e.g. &#x60;Europe/London&#x60;) this person prefers, or null for no explicit choice — the same shape as {@see self::$locale}: null is not UTC, it is \&quot;let the cascade decide\&quot; (cookie written by the browser&#39;s own auto-detection, then the instance default). A plain validated string rather than a backed enum like {@see self::$theme}/{@see self::$locale}: the IANA database has ~400 identifiers, too many for an enum to curate the way {@see \\App\\Enum\\Locale} deliberately does for its two cases. See {@see \\App\\Service\\TimezoneResolver}. | [optional] 
**password** | **str** | Hashed password; null for accounts that authenticate only via OAuth or LDAP. | [optional] 
**ldap_dn** | **str** | The bound entry&#39;s distinguished name in LLDAP. Presence means the account is LDAP-authoritative: {@see App\\Service\\LdapAccountLinker} clears any local password when it sets this, and it is never set alongside one. | [optional] 
**avatar_photo** | [**UserAvatarPhoto**](UserAvatarPhoto.md) |  | [optional] 
**roles** | **List[str]** |  | [optional] 
**disabled_at** | **datetime** | Set when a platform operator suspends the account; null &#x3D; active. | [optional] [readonly] 
**spam_marked_at** | **datetime** | When an operator judged this account to be spam; null &#x3D; not spam. | [optional] [readonly] 
**spam_marked_by** | [**User**](User.md) |  | [optional] 
**approved_at** | **datetime** | When an operator approved the account; null means it is still waiting and can reach nothing but the holding page ({@see self::getRoles()}). | [optional] [readonly] 
**email_confirmed_at** | **datetime** | When the address on this account was proven to be one the person can read; null means it never was ({@see \\App\\Service\\EmailConfirmationService}). | [optional] [readonly] 
**credit_granted_at** | **datetime** | When the one-off signup credit was granted ({@see \\App\\Service\\Credit\\SignupGrant}). | [optional] [readonly] 
**tier_pin** | **str** | An operator&#39;s override of the trust tier this account would otherwise progress into on its own; null means the automatic rule decides ({@see \\App\\Service\\Trust\\TierResolver}). | [optional] [readonly] 
**tier_pinned_at** | **datetime** |  | [optional] [readonly] 
**tier_pinned_by** | [**User**](User.md) |  | [optional] 
**tier_pin_reason** | **str** |  | [optional] [readonly] 
**oauth_identities** | [**List[OAuthIdentity]**](OAuthIdentity.md) |  | [optional] 
**totp_secret** | **str** | The TOTP shared secret, **encrypted at rest** ({@see \\App\\Service\\TwoFactor\\TotpSecretCipher}), or null for an account that has not enabled a second factor. | [optional] 
**totp_secret_key_id** | **str** | Which key wrapped {@see self::$totpSecret}, so a key rotation can re-wrap it without users re-enrolling ({@see \\App\\Service\\TwoFactor\\TotpSecretCipher}). | [optional] [readonly] 
**totp_confirmed_at** | **datetime** | When the person proved the authenticator by entering a live code; null means 2FA is not in force for this account. This is the flag the step-up gate reads ({@see \\App\\EventSubscriber\\TwoFactorStepUpSubscriber}). | [optional] [readonly] 
**recovery_codes** | [**List[RecoveryCode]**](RecoveryCode.md) |  | [optional] 
**machine_for** | **str** | The organization this account exists to act for, or null for a person. | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**display_label** | **str** | How this person is named in the UI. Registration requires a display name, but an OAuth provider may not share one, so the handle stands in — never the email address, which is not ours to show. | [optional] [readonly] 
**machine** | **bool** | Whether this account is a machine acting for an organization, not a person. | [optional] [readonly] 
**ldap_managed** | **bool** |  | [optional] [readonly] 
**avatar_photo_type** | **str** |  | [optional] [readonly] 
**user_identifier** | **str** | The identifier stored in the session token. Sign-in accepts either the email or the username ({@see UserRepository::loadUserByIdentifier()}); this is the canonical one the token is refreshed from. | [optional] [readonly] 
**granted_roles** | **List[str]** | The roles the account actually carries, whether or not it has been approved — what the admin panel shows and what the feature toggles flip. | [optional] 
**disabled** | **bool** |  | [optional] [readonly] 
**spam** | **bool** |  | [optional] [readonly] 
**approved** | **bool** |  | [optional] [readonly] 
**email_confirmed** | **bool** |  | [optional] [readonly] 
**tier_pinned** | **bool** |  | [optional] [readonly] 
**totp_enabled** | **bool** | True once the person has proved the authenticator — the gate&#39;s on/off switch. | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.user import User

# TODO update the JSON string below
json = "{}"
# create an instance of User from a JSON string
user_instance = User.from_json(json)
# print the JSON string representation of the object
print(User.to_json())

# convert the object into a dict
user_dict = user_instance.to_dict()
# create an instance of User from a dict
user_from_dict = User.from_dict(user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


