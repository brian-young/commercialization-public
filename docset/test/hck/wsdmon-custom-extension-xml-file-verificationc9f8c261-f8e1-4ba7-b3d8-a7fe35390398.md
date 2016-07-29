---
author: joshbax-msft
title: WSDMon Custom Extension XML File Verification
description: WSDMon Custom Extension XML File Verification
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 1bb44f16-1e3f-4619-ac58-38264e94cb3d
---

# WSDMon Custom Extension XML File Verification


This automated test validates a printer driver's Web Services for Devices Port Monitor bidi extension file to verify that the file is well-formed and syntactically correct.

This test validates the custom extension file. The test deletes any .xml contents that the test deems are invalid. You can run the test against an installed printer or a static file. If you run the test against an installed printer, the test determines if the printer driver has a bidi extension file that is defined for the WSDMon port monitor. If the file is defined, the test loads and verifies the file. If the test is run against a static file, the test loads and verifies the specified file.

For Windows Vista, an IHV can customize the Web Services for Devices port monitor (WSDMon) by creating a bidi extension file. This is an XML file that defines new schemas that are specific to the IHV driver by using using constructs of the WSDMon XSD file. This test validates the custom extension file against the XSD file. The test can be run against an installed printer or against a specific file. If the test is run against an installed printer, the test tries to validate the custom extension file defined in the printer’s dependent file list. If the printer does not have a custom extension file, the test will pass without error. If the test is run against a specific file, it just validates the named file against the WSDMon XSD file.

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.Imaging.Printer.Base.autoConfiguration</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows 7 (x64) Windows 7 (x86) Windows 8 (x64) Windows 8 (x86) Windows Server 2012 (x64) Windows Server 2008 R2 (x64) Windows 8.1 x64 Windows 8.1 x86 Windows Server 2012 R2</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~1 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification Functional</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Automated</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in the test requirements: [Printer Testing Prerequisites](printer-testing-prerequisites.md).

## Troubleshooting


For troubleshooting information, see [Troubleshooting Device.Imaging Testing](troubleshooting-deviceimaging-testing.md).

 

 





