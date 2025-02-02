---
title: DeviceCompanionApplications
description: DeviceCompanionApplications
ms.date: 04/20/2017
---

# DeviceCompanionApplications

[!include[MBAE deprecation warning](../includes/mbae-deprecation-warning.md)]

The DeviceCompanionApplications element specifies the app that will be downloaded when the operator’s mobile broadband hardware is detected on the PC.

## Usage


``` syntax
<DeviceCompanionApplications>
  child elements
</DeviceCompanionApplications>
```

## Attributes


There are no attributes.

## Child elements


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="package.md" data-raw-source="[Package](package.md)">Package</a></p></td>
<td><p>Specifies the package that will be used for the Microsoft Store device app.</p></td>
</tr>
</tbody>
</table>

 

## Parent elements


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="softwareinfo.md" data-raw-source="[SoftwareInfo](softwareinfo.md)">SoftwareInfo</a></p></td>
<td><p>The parent element of the <a href="softwareinfo-xml-schema.md" data-raw-source="[SoftwareInfo XML schema](softwareinfo-xml-schema.md)">SoftwareInfo XML schema</a>.</p></td>
</tr>
</tbody>
</table>

 

## XSD


``` syntax
<xs:element name="DeviceCompanionApplications" type="tns:DeviceCompanionApplicationsType" />

<xs:complexType name="DeviceCompanionApplicationsType">
  <xs:sequence>
    <xs:element name="Package" type="tns:PackageType" maxOccurs="unbounded" />
    <xs:any namespace="##other" processContents="lax" minOccurs="0" maxOccurs="unbounded" />
  </xs:sequence>
</xs:complexType>
```

## Remarks


-   When you specify the DeviceCompanionApplications element, the specified app will be downloaded when Windows detects the operator’s mobile broadband hardware.

-   The structure for the package [Identity](identity.md) and [Application](application-softwareinfo-schema.md) element are identical with the application manifest structure.

-   For Windows 8, Windows 8.1, and Windows 10, you can specify only one package and one application ID. The second package or application ID will be ignored if you specify it.

The DeviceCompanionApplications element is optional.

 

 





