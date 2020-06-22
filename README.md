# Send png image as a result


```scala

import org.apache.commons.io.IOUtils

complete(ToResponseMarshallable(
    HttpEntity(MediaTypes.`image/png`,
        IOUtils.toByteArray(getClass.getClassLoader.getResource("images/image.png"))
    )
)
(
    PredefinedToResponseMarshallers.fromToEntityMarshaller()(PredefinedToEntityMarshallers.MessageEntityMarshaller)
))
```
