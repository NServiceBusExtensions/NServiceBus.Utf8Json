<img src="/src/icon.png" height="25px"> Add support for [NServiceBus](https://particular.net/NServiceBus) message serialization via [Utf8Json](https://github.com/neuecc/Utf8Json)

<!--- StartOpenCollectiveBackers -->

[Already a Patron? skip past this section](#endofbacking)


## Community backed

**It is expected that all developers [become a Patron](https://opencollective.com/nservicebusextensions/order/6976) to use any of these libraries. [Go to licensing FAQ](https://github.com/NServiceBusExtensions/Home/blob/master/readme.md#licensingpatron-faq)**


### Sponsors

Support this project by [becoming a Sponsors](https://opencollective.com/nservicebusextensions/order/6972). The company avatar will show up here with a link to your website. The avatar will also be added to all GitHub repositories under this organization.


### Patrons

Thanks to all the backing developers! Support this project by [becoming a patron](https://opencollective.com/nservicebusextensions/order/6976).

<img src="https://opencollective.com/nservicebusextensions/tiers/patron.svg?width=890&avatarHeight=60&button=false">

<!--- EndOpenCollectiveBackers -->

<a href="#" id="endofbacking"></a>

## NuGet package

https://nuget.org/packages/NServiceBus.Utf8Json/ [![NuGet Status](https://img.shields.io/nuget/v/NServiceBus.Utf8Json.svg?style=flat&max-age=86400)](https://www.nuget.org/packages/NServiceBus.Utf8Json/)


## Usage

snippet: Utf8JsonSerialization


### Resolver

It is possible to customize the instance of [IJsonFormatterResolver](https://github.com/neuecc/Utf8Json#resolver) used for serialization.

snippet: Utf8JsonResolver

include: custom-contenttype-key

snippet: Utf8JsonContentTypeKey


## Currently not supported

The use of `DataBusProperty<T>` is not supported because the property doesn't provide a default constructor. However, the use of the [databus conventions](/nservicebus/messaging/databus) is supported.



## Icon

[Fractal](https://thenounproject.com/term/fractal/26234/) designed by [Yi Chen](https://thenounproject.com/jsczcy/) from [The Noun Project](https://thenounproject.com).