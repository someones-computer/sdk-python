# Service


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deployment** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**image** | **str** |  | [optional] 
**replicas** | **int** |  | [optional] [default to 1]
**cpu_limit** | [**ServiceCpuLimit**](ServiceCpuLimit.md) |  | [optional] 
**mem_limit** | [**ServiceMemLimit**](ServiceMemLimit.md) |  | [optional] 
**cpu_reservation** | [**ServiceCpuReservation**](ServiceCpuReservation.md) |  | [optional] 
**mem_reservation** | [**ServiceMemReservation**](ServiceMemReservation.md) |  | [optional] 
**ports** | **List[Dict[str, ServicePortsInnerValue]]** |  | [optional] 
**http_port** | **int** | The container port this service speaks HTTP on, as compose&#39;s &#x60;x-someones.http&#x60; declared it — null means nothing was declared and {@see \\App\\Service\\Ingress\\IngressPlanner} falls back to the well-known ports. | [optional] 
**command** | **List[str]** | The container&#39;s argv, as compose &#x60;command:&#x60; declared it — already split into words by the parser, because Swarm&#39;s &#x60;Args&#x60; is argv rather than a line. | [optional] 
**entrypoint** | **List[str]** | The container&#39;s &#x60;Command&#x60; — compose &#x60;entrypoint:&#x60;, which replaces the image&#39;s own &#x60;ENTRYPOINT&#x60; rather than feeding it, unlike {@see $command}. | [optional] 
**healthcheck** | [**Dict[str, ServiceHealthcheckValue]**](ServiceHealthcheckValue.md) | Compose &#x60;healthcheck:&#x60;, projected straight from {@see \\App\\Service\\Compose\\ComposeParser::healthcheck()} into the shape {@see \\App\\Service\\Deploy\\StackDeployer} sends as Swarm&#39;s &#x60;ContainerSpec.Healthcheck&#x60; — &#x60;test&#x60; is a &#x60;NONE&#x60;/&#x60;CMD&#x60;/&#x60;CMD-SHELL&#x60; argv, the rest are nanoseconds/a count. Null means nothing was declared, so an image&#39;s own baked-in &#x60;HEALTHCHECK&#x60; (or none) stands; &#x60;disable: true&#x60; in the compose file is not null, it is &#x60;test: [\&quot;NONE\&quot;]&#x60; — an explicit instruction rather than silence. | [optional] 
**restart** | **str** | What happens when a container exits; also decides service vs job. | [optional] [default to 'always']
**forwarded_unscanned** | **bool** | Set while this service&#39;s image arrived by client-side forwarding (docs/registry.md&#39;s \&quot;Client-side forwarding\&quot; callout) and no scan verdict is yet on record for the digest it was pinned to — bytes from a user&#39;s machine, not a source tree we built or a registry we chose to trust. A forwarded image is scanned as it loads ({@see \\App\\MessageHandler\\BuildBundleHandler}), so this is normally cleared by the time the service is projected; one left set is a forwarded image that reached deploy unvetted, which {@see \\App\\MessageHandler\\DeployRevisionHandler} refuses to run (docs/image-scanning.md). | [optional] [default to False]
**id** | **str** |  | [optional] [readonly] 
**created_at** | **datetime** |  | [optional] [readonly] 
**updated_at** | **datetime** |  | [optional] [readonly] 

## Example

```python
from someones_computer_sdk.models.service import Service

# TODO update the JSON string below
json = "{}"
# create an instance of Service from a JSON string
service_instance = Service.from_json(json)
# print the JSON string representation of the object
print(Service.to_json())

# convert the object into a dict
service_dict = service_instance.to_dict()
# create an instance of Service from a dict
service_from_dict = Service.from_dict(service_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


