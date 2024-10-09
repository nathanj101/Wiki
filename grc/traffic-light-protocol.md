---
icon: traffic-light
---

# Traffic Light Protocol

## Introduction <a href="#introduction" id="introduction"></a>

The Traffic Light Protocol (TLP) version 2.0 is a set of designations used to ensure that sensitive information is shared securely and appropriately. It originated in the intelligence community but has since been adopted by various organisations, including government agencies and private corporations, to facilitate the sharing of sensitive information while maintaining control over its distribution.

The choice of using colours mirrors the intuitive and universally recognised nature of traffic lights. These colours—red, amber (or yellow), and green—carry specific meanings that are easily understood, aiding in the swift comprehension of the sensitivity levels associated with shared information, irrespective of language or cultural background.

## Rules <a href="#rules" id="rules"></a>

* The four TLP labels are: **TLP:RED, TLP:AMBER, TLP:GREEN, and TLP:CLEAR**.
* Must not contain spaces.
* Must be in capitals.
* Must remain in their original form, even when used in other languages.
* If a recipient needs to share information more widely than indicated by the TLP label it came with, they must obtain explicit permission from the source.
* The source is responsible for ensuring that recipients of TLP-labelled information understand and can follow TLP sharing guidance.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

## Definitions <a href="#definitions" id="definitions"></a>

**Community:** Under TLP, a community is a group who share common goals, practices, and informal trust relationships. A community can be as broad as all cybersecurity practitioners in a country (or in a sector or region).

**Organisation:** Under TLP, an organisation is a group who share a common affiliation by formal membership and are bound by common policies set by the organisation. An organisation can be as broad as all members of an information sharing organisation, but rarely broader.

**Clients:** Under TLP, clients are those people or entities that receive cybersecurity services from an organisation. Clients are by default included in TLP:AMBER so that the recipients may share information further downstream in order for clients to take action to protect themselves. For teams with national responsibility this definition includes stakeholders and constituents.

{% tabs %}
{% tab title="TLP:CLEAR" %}
<div align="left">

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>

Recipients can spread this to the _world_, there is no limit on disclosure. Sources may use TLP:CLEAR when information carries minimal or no foreseeable risk of misuse, in accordance with applicable rules and procedures for public release. Subject to standard copyright rules, TLP:CLEAR information may be shared without restriction.&#x20;
{% endtab %}

{% tab title="TLP:GREEN" %}
<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Limited disclosure, recipients can spread this within their community. Sources may use TLP:GREEN when information is useful to increase awareness within their wider community. Recipients may share TLP:GREEN information with peers and partner organisations within their community, but not via publicly accessible channels. TLP:GREEN information may not be shared outside of the community. Note: when “community” is not defined, assume the cybersecurity/defence community.
{% endtab %}

{% tab title="TLP:AMBER" %}
<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Limited disclosure, recipients can only spread this on a need-to-know basis within their _organisation_ and its _clients_. Note that **TLP:AMBER+STRICT** restricts sharing to the _organisation_ only. Sources may use TLP:AMBER when information requires support to be effectively acted upon, yet carries risk to privacy, reputation, or operations if shared outside of the organisations involved. Recipients may share TLP:AMBER information with members of their own organisation and its clients, but only on a need-to-know basis to protect their organisation and its clients and prevent further harm. Note: if the source wants to restrict sharing to the organisation **only**, they must specify TLP:AMBER+STRICT.
{% endtab %}

{% tab title="TLP:RED" %}
<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

For the eyes and ears of _individual_ recipients only, no further disclosure. Sources may use TLP:RED when information cannot be effectively acted upon without significant risk for the privacy, reputation, or operations of the organisations involved. Recipients may therefore not share TLP:RED information with anyone else. In the context of a meeting, for example, TLP:RED information is limited to those present at the meeting.
{% endtab %}
{% endtabs %}

## Usage <a href="#usage" id="usage"></a>

**Email and IM:** TLP-labelled messaging MUST indicate the TLP label of the information, as well as any additional restrictions, directly prior to the information itself. The TLP label SHOULD be in the subject line of email. Where needed, also make sure to designate the end of the text to which the TLP label applies.

_Example:_

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**Official Documents:** TLP-labelled documents MUST indicate the TLP label of the information, as well as any additional restrictions, in the header and footer of each page. The TLP label SHOULD be in 12-point type or greater for users with low vision.

_Example:_

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

## References <a href="#references" id="references"></a>

https://www.first.org/tlp/\
https://www.cisa.gov/news-events/news/traffic-light-protocol-tlp-definitions-and-usage
