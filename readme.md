<!--
GENERATED FILE - DO NOT EDIT
This file was generated by [MarkdownSnippets](https://github.com/SimonCropp/MarkdownSnippets).
Source File: /readme.source.md
To change this file edit the source file and then run MarkdownSnippets.
-->

# <img src="/src/icon.png" height="30px"> NServiceBus.Utf8Json

[![Build status](https://ci.appveyor.com/api/projects/status/oiqo5mrf54mh9iu8/branch/master?svg=true)](https://ci.appveyor.com/project/SimonCropp/nservicebus-Utf8Json)
[![NuGet Status](https://img.shields.io/nuget/v/NServiceBus.Utf8Json.svg)](https://www.nuget.org/packages/NServiceBus.Utf8Json/)


Add support for [NServiceBus](https://particular.net/NServiceBus) message serialization via [Utf8Json](https://github.com/neuecc/Utf8Json)

<!-- toc -->
## Contents

  * [Community backed](#community-backed)
    * [Sponsors](#sponsors)
    * [Patrons](#patrons)
  * [Usage](#usage)
    * [Resolver](#resolver)
    * [Custom content key](#custom-content-key)
  * [Currently not supported](#currently-not-supported)<!-- endtoc -->

<!--- StartOpenCollectiveBackers -->

[Already a Patron? skip past this section](#endofbacking)


## Community backed

**It is expected that all developers [become a Patron](https://opencollective.com/nservicebusextensions/order/6976) to use any of these libraries. [Go to licensing FAQ](https://github.com/NServiceBusExtensions/Home/#licensingpatron-faq)**


### Sponsors

Support this project by [becoming a Sponsors](https://opencollective.com/nservicebusextensions/order/6972). The company avatar will show up here with a link to your website. The avatar will also be added to all GitHub repositories under this organization.


### Patrons

Thanks to all the backing developers! Support this project by [becoming a patron](https://opencollective.com/nservicebusextensions/order/6976).

<img src="https://opencollective.com/nservicebusextensions/tiers/patron.svg?width=890&avatarHeight=60&button=false">

<!--- EndOpenCollectiveBackers -->

<a href="#" id="endofbacking"></a>


## NuGet package

https://nuget.org/packages/NServiceBus.Utf8Json/


## Usage

<!-- snippet: Utf8JsonSerialization -->
<a id='snippet-utf8jsonserialization'/></a>
```cs
configuration.UseSerialization<Utf8JsonSerializer>();
```
<sup><a href='/src/Tests/Snippets/Usage.cs#L9-L13' title='File snippet `utf8jsonserialization` was extracted from'>snippet source</a> | <a href='#snippet-utf8jsonserialization' title='Navigate to start of snippet `utf8jsonserialization`'>anchor</a></sup>
<!-- endsnippet -->


### Resolver

It is possible to customize the instance of [IJsonFormatterResolver](https://github.com/neuecc/Utf8Json#resolver) used for serialization.

<!-- snippet: Utf8JsonResolver -->
<a id='snippet-utf8jsonresolver'/></a>
```cs
var serialization = configuration.UseSerialization<Utf8JsonSerializer>();
serialization.Resolver(StandardResolver.SnakeCase);
```
<sup><a href='/src/Tests/Snippets/Usage.cs#L18-L23' title='File snippet `utf8jsonresolver` was extracted from'>snippet source</a> | <a href='#snippet-utf8jsonresolver' title='Navigate to start of snippet `utf8jsonresolver`'>anchor</a></sup>
<!-- endsnippet -->


### Custom content key

When using [additional deserializers](https://docs.particular.net/nservicebus/serialization/#specifying-additional-deserializers) or transitioning between different versions of the same serializer it can be helpful to take explicit control over the content type a serializer passes to NServiceBus (to be used for the [ContentType header](https://docs.particular.net/nservicebus/messaging/headers#serialization-headers-nservicebus-contenttype)).

<!-- snippet: Utf8JsonContentTypeKey -->
<a id='snippet-utf8jsoncontenttypekey'/></a>
```cs
var serialization = configuration.UseSerialization<Utf8JsonSerializer>();
serialization.ContentTypeKey("custom-key");
```
<sup><a href='/src/Tests/Snippets/Usage.cs#L28-L33' title='File snippet `utf8jsoncontenttypekey` was extracted from'>snippet source</a> | <a href='#snippet-utf8jsoncontenttypekey' title='Navigate to start of snippet `utf8jsoncontenttypekey`'>anchor</a></sup>
<!-- endsnippet -->


## Currently not supported

The use of `DataBusProperty<T>` is not supported because the property doesn't provide a default constructor. However, the use of the [databus conventions](https://docs.particular.net/nservicebus/messaging/databus) is supported.


## Release Notes

See [closed milestones](../../milestones?state=closed).


## Icon

[Fractal](https://thenounproject.com/term/fractal/26234/) designed by [Yi Chen](https://thenounproject.com/jsczcy/) from [The Noun Project](https://thenounproject.com).
