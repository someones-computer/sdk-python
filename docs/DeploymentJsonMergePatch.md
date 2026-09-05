# DeploymentJsonMergePatch

An IMMUTABLE compose revision. A deploy is a new row; rollback re-points Application::$currentDeployment at an older one. Placement is resolved onto this row (targetSwarm) at deploy time, so migration is just the next revision.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | [optional] 
**sequence** | **int** | Monotonic per-application revision number. | [optional] 
**name** | **str** | What this revision is called — &#x60;sc&#x60; defaults it to the slugified branch, so the normal shape is a deployment per branch. Null for revisions created before the field existed, or by a client that doesn&#39;t send one. | [optional] 
**raw_compose** | **str** | Exactly what the user submitted. | [optional] 
**canonical_spec** | [**Dict[str, DeploymentJsonMergePatchCanonicalSpecValue]**](DeploymentJsonMergePatchCanonicalSpecValue.md) | Parsed, supported-subset-only canonical representation — what {@see \\App\\Service\\Compose\\ComposeParser::parse()} produced. Both keys are optional here and not there: a row is whatever was written when it was written, so a revision that predates a key still has to load. | [optional] 
**build_contexts** | **Dict[str, Dict[str, DeploymentJsonMergePatchBuildContextsValueValue]]** | Build contexts uploaded with this revision, keyed by compose service name: &#x60;{ contextSha256, dockerfile, dockerfileContent?, additionalContexts?, image?, log? }&#x60;. The tarballs themselves live in the content-addressed bundle cache ({@see \\App\\Service\\Bundle\\BundleStorage}); this is the pointer the build worker will walk. &#x60;dockerfileContent&#x60; is a best-effort text preview extracted at ingest ({@see \\App\\Service\\Bundle\\ContextDockerfileReader}) — null when the context was too large to preview or predates this field. | [optional] 
**forwarded_images** | **Dict[str, Dict[str, Optional[str]]]** | Client-forwarded images uploaded with this revision, keyed by compose service name: &#x60;{ contextSha256, originalImage, image?, log? }&#x60;. See docs/registry.md&#39;s \&quot;Client-side forwarding\&quot; callout: &#x60;sc&#x60; detects a private, unbuildable &#x60;image:&#x60; reference it can already reach locally and offers to upload it, for a platform that has no other way to pull it. A sibling to {@see self::$buildContexts} rather than folded into it — that array means \&quot;run this through BuildKit\&quot;, and this one never does. The tarballs live in the object store ({@see \\App\\Service\\Bundle\\ImageStorage}), not the database; &#x60;image&#x60; is filled in once the loader has pushed it to the internal registry, the same way &#x60;buildContexts[][&#39;image&#39;]&#x60; is. &#x60;{}&#x60; for every revision that forwarded nothing, which is most of them. | [optional] 
**build_secrets** | **Dict[str, Dict[str, Dict[str, str]]]** | &#x60;build.secrets&#x60; values declared for this revision&#39;s build services (Grey.ooo/someones.computer_agent#46), sealed the moment they arrive ({@see \\App\\Service\\Secret\\SecretBox}) and never written to the object store the way a build context is: unlike a context tarball, a build secret is live tenant credential material, not something worth caching by content — closer to how {@see \\App\\Service\\Registry\\RegistryTokenSigner} mints a push token than to how {@see \\App\\Entity\\Variable} keeps one. | [optional] 
**target_swarm** | **str** | Resolved by the placement engine; null until placed. | [optional] 
**status** | **str** |  | [optional] [default to 'pending']
**status_reason** | **str** | Why the revision is in its current status — the build worker&#39;s failure message, typically. Null whenever there is nothing to explain. | [optional] 
**failed_on_swarm** | **bool** | Set on a &#x60;Failed&#x60; revision that had already created or updated at least one service on &#x60;$targetSwarm&#x60; before the failure — a live half-stack, not \&quot;nothing happened\&quot; (#1270). {@see self::isOnASwarm()} reads this for exactly the revisions the ordinary &#x60;Deploying&#x60;/&#x60;Running&#x60; check cannot see: whatever partially landed still has to be reachable to a manual Teardown and countable by the stray-container sweep, which is why every other status leaves this false rather than tracking it. | [optional] [default to False]
**zero_task_observed_at** | **datetime** | When {@see \\App\\Service\\Reconcile\\RevisionDegradationDetector} first found this &#x60;Running&#x60; revision with no task actually running on its swarm — null while at least one is, or before it was ever checked. | [optional] 
**degraded** | **bool** | Set once a &#x60;Running&#x60; revision has gone a full grace period with zero tasks actually running on its swarm (#1279) — a {@see Failure} of {@see \\App\\Enum\\FailurePhase::Runtime} is recorded alongside it. Never flips &#x60;$status&#x60; itself: &#x60;running&#x60; still means \&quot;this is what the application should be serving\&quot;, and a revision the platform cannot reach a running task for is a fact about the swarm, not a new desired state — the same desired/observed separation {@see \\App\\Service\\Reconcile\\DriftDetector} already keeps at read time, made durable here so it survives past one page view. | [optional] [default to False]
**digest** | **str** | Content digest of the canonical spec, for dedupe/audit. | [optional] 
**created_by** | [**User**](User.md) |  | [optional] 
**services** | [**List[Service]**](Service.md) |  | [optional] 
**variables** | [**List[DeploymentVariable]**](DeploymentVariable.md) |  | [optional] 
**failures** | [**List[Failure]**](Failure.md) |  | [optional] 
**id** | **str** |  | [optional] [readonly] 
**deleted_at** | **datetime** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 
**on_a_swarm** | **bool** | Whether this revision has a stack of its own on a swarm right now. | [optional] [readonly] 
**deleted** | **bool** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.deployment_json_merge_patch import DeploymentJsonMergePatch

# TODO update the JSON string below
json = "{}"
# create an instance of DeploymentJsonMergePatch from a JSON string
deployment_json_merge_patch_instance = DeploymentJsonMergePatch.from_json(json)
# print the JSON string representation of the object
print(DeploymentJsonMergePatch.to_json())

# convert the object into a dict
deployment_json_merge_patch_dict = deployment_json_merge_patch_instance.to_dict()
# create an instance of DeploymentJsonMergePatch from a dict
deployment_json_merge_patch_from_dict = DeploymentJsonMergePatch.from_dict(deployment_json_merge_patch_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


