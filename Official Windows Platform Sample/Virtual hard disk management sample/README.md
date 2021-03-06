# Virtual hard disk management sample
## Requires
- Visual Studio 2010
## License
- MS-LPL
## Technologies
- Win32
## Topics
- Hyper-V
## Updated
- 08/15/2012
## Description
<style> pre.syntax { font-size: 110 background: #dddddd; padding: 4px,8px; cursor: text; color: #000000; width: 97 } body{font-family:Verdana,Arial,Helvetica,sans-serif;color:#000;font-size:80%} H1{font-size:150%;font-weight:bold} H1.heading{font-size:110%;font-family:Verdana,Arial,Helvetica,sans-serif;font-weight:bold;line-height:120%}
 H2{font-size:115%;font-weight:700} H2.subtitle{font-size:180%;font-weight:400;margin-bottom:.6em} H3{font-size:110%;font-weight:700} H4,H5,H6{font-size:100%;font-weight:700} h4.subHeading{font-size:100%} dl{margin:0 0 10px;padding:0 0 0 1px} dt{font-style:normal;margin:0}
 li{margin-bottom:3px;margin-left:0} ol{line-height:140%;list-style-type:decimal;margin-bottom:15px;margin-left:24px} ol ol{line-height:140%;list-style-type:lower-alpha;margin-bottom:4px;margin-left:24px;margin-top:3px} ol ul,ul ol{line-height:140%;margin-bottom:15px;margin-top:15px}
 p{margin:0 0 10px;padding:0} div.section p{margin-bottom:15px;margin-top:0} ul{line-height:140%;list-style-position:outside;list-style-type:disc;margin-bottom:15px} ul ul{line-height:140%;list-style-type:disc;margin-bottom:4px;margin-left:17px;margin-top:3px}
 .heading{font-weight:700;margin-bottom:8px;margin-top:18px} .subHeading{font-size:100%;font-weight:700;margin:0} div#mainSection table{border:1px solid #ddd;font-size:100%;margin-bottom:5px;margin-left:5px;margin-top:5px;width:97%;clear:both} div#mainSection
 table tr{vertical-align:top} div#mainSection table th{border-bottom:1px solid #c8cdde;color:#006;padding-left:5px;padding-right:5px;text-align:left} div#mainSection table td{border:1px solid #d5d5d3;margin:1px;padding-left:5px;padding-right:5px} div#mainSection
 table td.imageCell{white-space:nowrap} /* These are the original lines from global-bn1945 div.ContentArea table th,div.ContentArea table td{background:#fff;border:0 solid #ccc;font-family:Verdana;padding:5px;text-align:left;vertical-align:top} div.ContentArea
 table th{background:#ccc none repeat scroll 0% 50%;vertical-align:bottom} div.ContentArea table{border-collapse:collapse;width:auto} */ /* Removing ContentArea class requirement from commented out lines from global-bn1945 above */ table th,table td{background:#fff;border:0
 solid #ccc;font-family:Verdana;padding:5px;text-align:left;vertical-align:top} table th{background:#ccc none repeat scroll 0% 50%;vertical-align:bottom} table{border-collapse:collapse;width:auto} div.clsNote{background-color:#eee;margin-bottom:4px;padding:2px}
 div.code{width:98.9%} code{font-family:Monospace,Courier New,Courier;font-size:105%;color:#006} span.label{font-weight:bold} div.caption{font-weight:bold;font-size:100%;color:#039} .procedureSubHeading{font-size:110%;font-weight:bold} span.sub{vertical-align:sub}
 span.sup{vertical-align:super} span.big{font-size:larger} span.small{font-size:smaller} span.tt{font-family:Courier,"Courier New",Consolas,monospace} .CCE_Message{color:Red;font-size:10pt} </style>
<div id="mainSection">
<p>This sample demonstrates how to use the Hyper-V WMI APIs and Virtual Hard Disk APIs to manage virtual hard disks.
</p>
<p>The Windows Samples Gallery contains a variety of code samples that demonstrate the use of various new programming features for managing Hyper-V that are available in Windows&nbsp;8 and/or Windows Server&nbsp;2012. These downloadable samples are provided as compressed
 ZIP files that contain a Microsoft Visual Studio&nbsp;2010 solution (SLN) file for the sample, along with the source files, assets, resources, and metadata necessary to successfully compile and run the sample. For more information about the programming models,
 platforms, languages, and APIs demonstrated in this sample, please refer to the <a href="http://msdn.microsoft.com/en-us/library/Hh850319">
Hyper-V WMI provider (V2)</a> documentation.</p>
<p>To obtain an evaluation copy of Windows&nbsp;8, go to <a href="http://go.microsoft.com/fwlink/?LinkId=241655">
Windows&nbsp;8</a>.</p>
<h3>Related technologies</h3>
<a href="http://msdn.microsoft.com/en-us/library/Hh850319">Hyper-V WMI provider (V2)</a>,
<a href="http://msdn.microsoft.com/en-us/library/windows/desktop/Dd323653">Virtual Storage</a>
<h3>Operating system requirements</h3>
<table>
<tbody>
<tr>
<th>Client</th>
<td><dt>Windows&nbsp;8 </dt></td>
</tr>
<tr>
<th>Server</th>
<td><dt>Windows Server&nbsp;2012 </dt></td>
</tr>
</tbody>
</table>
<h3>Build the sample</h3>
<h3><a id="Building_the_C__version_of_the_sample"></a><a id="building_the_c__version_of_the_sample"></a><a id="BUILDING_THE_C__VERSION_OF_THE_SAMPLE"></a>Building the C# version of the sample</h3>
<ol>
<li>
<p>Start Visual Studio and select <b>File</b> &gt; <b>Open</b> &gt; <b>Project/Solution</b>.</p>
</li><li>
<p>Go to the directory in which you unzipped the sample. Go to the directory named for the sample, and double-click the Microsoft Visual Studio Solution (.sln) file titled Storage.sln from Visual Studio&nbsp;2010.</p>
</li><li>
<p>Press F7 (or F6 for Microsoft Visual Studio Ultimate&nbsp;2012) or use <b>Build</b> &gt;
<b>Build Solution</b> to build the sample.</p>
</li></ol>
<h3><a id="Building_the_C___version_of_the_sample"></a><a id="building_the_c___version_of_the_sample"></a><a id="BUILDING_THE_C___VERSION_OF_THE_SAMPLE"></a>Building the C&#43;&#43; version of the sample</h3>
<ol>
<li>
<p>Start Visual Studio&nbsp;2010 and select <b>File</b> &gt; <b>Open</b> &gt; <b>Project/Solution</b>.</p>
</li><li>
<p>Go to the directory in which you unzipped the sample. Go to the directory named for the sample, and double-click the Microsoft Visual Studio Solution (.sln) file titled Storage.sln.</p>
</li><li>
<p>Press F7 (or F6 for Visual Studio Ultimate&nbsp;2012) or use <b>Build</b> &gt; <b>Build Solution</b> to build the sample.</p>
</li></ol>
<h3>Run the sample</h3>
<h3><a id="Running_the_C__version_of_the_sample"></a><a id="running_the_c__version_of_the_sample"></a><a id="RUNNING_THE_C__VERSION_OF_THE_SAMPLE"></a>Running the C# version of the sample</h3>
<p class="note"><b>Note</b>&nbsp;&nbsp;This sample must be run as an administrator.</p>
<p>This sample is written in C# using the Hyper-V WMI APIs, and requires some experience with WMI programming.</p>
<p>This sample can be run in several different modes.</p>
<h4><a id="Retrieve_information_about_a_virtual_hard_disk"></a><a id="retrieve_information_about_a_virtual_hard_disk"></a><a id="RETRIEVE_INFORMATION_ABOUT_A_VIRTUAL_HARD_DISK"></a>Retrieve information about a virtual hard disk</h4>
<p>To retrieve information about a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850064">
<b>GetVirtualHardDiskSettingData</b> </a>and <a href="http://msdn.microsoft.com/en-us/library/Hh850065">
<b>GetVirtualHardDiskState</b> </a>methods, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe GetVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Modify_the_settings_of__a_virtual_hard_disk"></a><a id="modify_the_settings_of__a_virtual_hard_disk"></a><a id="MODIFY_THE_SETTINGS_OF__A_VIRTUAL_HARD_DISK"></a>Modify the settings of a virtual hard disk</h4>
<p>To modify the settings of a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850302">
<b>SetVirtualHardDiskSettingData</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe SetVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
<b></b><i>ParentPath</i> <b></b><i>Format</i> <b></b><i>FileSize</i> <b></b><i>BlockSize</i>
<b></b><i>SectorSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file to be modified. </li><li><i>ParentPath</i> is the new path of the parent virtual hard disk file. </li><li><i>Format</i> is &quot;vhdx&quot; to make the virtual hard disk a VHDX or &quot;vhd&quot; to make the virtual hard disk a VHD.
</li><li><i>FileSize</i> is the new maximum size of the virtual hard disk, in bytes. </li><li><i>BlockSize</i> is the new block size of the virtual hard disk, in bytes. </li><li><i>SectorSize</i> is the new sector size of the virtual hard disk, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Validate_a_virtual_hard_disk"></a><a id="validate_a_virtual_hard_disk"></a><a id="VALIDATE_A_VIRTUAL_HARD_DISK"></a>Validate a virtual hard disk</h4>
<p>To validate a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850312">
<b>ValidateVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe ValidateVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create__a_fixed_virtual_hard_disk"></a><a id="create__a_fixed_virtual_hard_disk"></a><a id="CREATE__A_FIXED_VIRTUAL_HARD_DISK"></a>Create a fixed virtual hard disk</h4>
<p>To create a fixed virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850039">
<b>CreateVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe CreateFixedVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
<b></b><i>Format</i> <b></b><i>FileSize</i> <b></b><i>BlockSize</i> <b></b><i>SectorSize</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file to be created. </li><li><i>Format</i> is &quot;vhdx&quot; to make the new virtual hard disk a VHDX or &quot;vhd&quot; to make the new virtual hard disk a VHD.
</li><li><i>FileSize</i> is the maximum size of the virtual hard disk, in bytes. </li><li><i>BlockSize</i> is the block size of the virtual hard disk, in bytes. </li><li><i>SectorSize</i> is the sector size of the virtual hard disk, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create__a_dynamic_virtual_hard_disk"></a><a id="create__a_dynamic_virtual_hard_disk"></a><a id="CREATE__A_DYNAMIC_VIRTUAL_HARD_DISK"></a>Create a dynamic virtual hard disk</h4>
<p>To create a dynamic virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850039">
<b>CreateVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe CreateDynamicVirtualHardDisk </b><i>ServerName</i> <b>
</b><i>VhdPath</i> <b></b><i>Format</i> <b></b><i>FileSize</i> <b></b><i>BlockSize</i>
<b></b><i>SectorSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file to be created. </li><li><i>Format</i> is &quot;vhdx&quot; to make the new virtual hard disk a VHDX or &quot;vhd&quot; to make the new virtual hard disk a VHD.
</li><li><i>FileSize</i> is the initial maximum size of the virtual hard disk, in bytes.
</li><li><i>BlockSize</i> is the block size of the virtual hard disk, in bytes. </li><li><i>SectorSize</i> is the sector size of the virtual hard disk, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create_a_differencing_virtual_hard_disk"></a><a id="create_a_differencing_virtual_hard_disk"></a><a id="CREATE_A_DIFFERENCING_VIRTUAL_HARD_DISK"></a>Create a differencing virtual hard disk</h4>
<p>To create a differencing virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850039">
<b>CreateVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe CreateDifferencingVirtualHardDisk </b><i>ServerName</i>
<b></b><i>VhdPath</i> <b></b><i>ParentPath</i> <b></b><i>Format</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the new virtual hard disk file. </li><li><i>ParentPath</i> is the path of the parent virtual hard disk file. </li><li><i>Format</i> is &quot;vhdx&quot; to make the new virtual hard disk a VHDX or &quot;vhd&quot; to make the new virtual hard disk a VHD.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create_a_virtual_floppy_disk"></a><a id="create_a_virtual_floppy_disk"></a><a id="CREATE_A_VIRTUAL_FLOPPY_DISK"></a>Create a virtual floppy disk</h4>
<p>To create a virtual floppy disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850038">
<b>CreateVirtualFloppyDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe CreateVirtualFloppyDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Attach_a_virtual_hard_disk"></a><a id="attach_a_virtual_hard_disk"></a><a id="ATTACH_A_VIRTUAL_HARD_DISK"></a>Attach a virtual hard disk</h4>
<p>To attach a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850023">
<b>AttachVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe AttachVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
<b></b><i>AssignDriveLetter</i> <b></b><i>ReadOnly</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file to be attached. </li><li><i>AssignDriveLetter</i> is &quot;True&quot; to automatically assign a drive letter to the attached drive or &quot;False&quot; otherwise.
</li><li><i>ReadOnly</i> is &quot;True&quot; to make the attached drive read only or &quot;False&quot; otherwise.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Detach_a_virtual_hard_disk"></a><a id="detach_a_virtual_hard_disk"></a><a id="DETACH_A_VIRTUAL_HARD_DISK"></a>Detach a virtual hard disk</h4>
<p>To detach a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850046">
<b>DetachVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe DetachVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Update_the_parent_of__a_virtual_hard_disk"></a><a id="update_the_parent_of__a_virtual_hard_disk"></a><a id="UPDATE_THE_PARENT_OF__A_VIRTUAL_HARD_DISK"></a>Update the parent of a virtual hard disk</h4>
<p>To update the parent of a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850298">
<b>SetParentVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe SetParentVirtualHardDisk </b><i>ServerName</i> <b></b><i>ChildPath</i>
<b></b><i>ParentPath</i> <b></b><i>LeafPath</i> <b></b><i>IgnoreIDMistmatch</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>ChildPath</i> is the path of the child virtual hard disk file. </li><li><i>ParentPath</i> is the path of the parent virtual hard disk file. </li><li><i>LeafPath</i> is the path of the leaf virtual hard disk file. </li><li><i>IgnoreIDMistmatch</i> is &quot;True&quot; to forcibly set the parent even if the identifiers do not match, or &quot;False&quot; otherwise.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Convert_a_virtual_hard_disk_to_fixed"></a><a id="convert_a_virtual_hard_disk_to_fixed"></a><a id="CONVERT_A_VIRTUAL_HARD_DISK_TO_FIXED"></a>Convert a virtual hard disk to fixed</h4>
<p>To convert a non-fixed virtual hard disk to fixed using the <a href="http://msdn.microsoft.com/en-us/library/Hh850035">
<b>ConvertVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe ConvertVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdSourcePath</i>
<b></b><i>VhdDestinationPath</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdSourcePath</i> is the path of the virtual hard disk file to be converted.
</li><li><i>VhdDestinationPath</i> is the destination path of the converted virtual hard disk file.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Merge_a_virtual_hard_disk"></a><a id="merge_a_virtual_hard_disk"></a><a id="MERGE_A_VIRTUAL_HARD_DISK"></a>Merge a virtual hard disk</h4>
<p>To merge a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850091">
<b>MergeVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe MergeVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdSourcePath</i>
<b></b><i>VhdDestinationPath</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdSourcePath</i> is the path of the virtual hard disk file to be merged. </li><li><i>VhdDestinationPath</i> is the destination path of the merged virtual hard disk file.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Compact_a_virtual_hard_disk"></a><a id="compact_a_virtual_hard_disk"></a><a id="COMPACT_A_VIRTUAL_HARD_DISK"></a>Compact a virtual hard disk</h4>
<p>To compact a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850033">
<b>CompactVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe CompactVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
<b></b><i>Mode</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>Mode</i> specifies the compaction mode and is one of the numeric values specified for the
<i>Mode</i> parameter of the <a href="http://msdn.microsoft.com/en-us/library/Hh850033">
<b>CompactVirtualHardDisk</b> </a>method. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Resize_a_virtual_hard_disk"></a><a id="resize_a_virtual_hard_disk"></a><a id="RESIZE_A_VIRTUAL_HARD_DISK"></a>Resize a virtual hard disk</h4>
<p>To resize a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh850285">
<b>ResizeVirtualHardDisk</b> </a>method, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>StorageSamplesWmi.exe ResizeVirtualHardDisk </b><i>ServerName</i> <b></b><i>VhdPath</i>
<b></b><i>NewSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>ServerName</i> is the name of the server on which to perform the operation.
</li><li><i>VhdPath</i> is the path of the virtual hard disk file to be resized. </li><li><i>NewSize</i> is the new maximum size of virtual hard disk file, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h3><a id="Running_the_C___version_of_the_sample"></a><a id="running_the_c___version_of_the_sample"></a><a id="RUNNING_THE_C___VERSION_OF_THE_SAMPLE"></a>Running the C&#43;&#43; version of the sample</h3>
<p class="note"><b>Note</b>&nbsp;&nbsp;This sample must be run as an administrator.</p>
<p>This sample is written in C&#43;&#43; using the Virtual Storage APIs and requires some experience with Windows API programming.</p>
<p>The sample demonstrates how to perform each of the following operations:</p>
<h4><a id="Retrieve_information_about_a_virtual_hard_disk"></a><a id="retrieve_information_about_a_virtual_hard_disk"></a><a id="RETRIEVE_INFORMATION_ABOUT_A_VIRTUAL_HARD_DISK"></a>Retrieve information about a virtual hard disk</h4>
<p>To retrieve information about a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323670">
<b>GetVirtualDiskInformation</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe GetVirtualDiskInformation </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create_a_fixed_virtual_hard_disk"></a><a id="create_a_fixed_virtual_hard_disk"></a><a id="CREATE_A_FIXED_VIRTUAL_HARD_DISK"></a>Create a fixed virtual hard disk</h4>
<p>To create a fixed virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323659">
<b>CreateVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe CreateFixedVirtualDisk </b><i>VhdPath</i> <b></b><i>FileSize</i>
<b></b><i>BlockSize</i> <b></b><i>SectorSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>FileSize</i> is the maximum size of the virtual hard disk. </li><li><i>BlockSize</i> is the block size of the virtual hard disk, in bytes. </li><li><i>SectorSize</i> is the sector size of the virtual hard disk, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create_a_dynamic_virtual_hard_disk"></a><a id="create_a_dynamic_virtual_hard_disk"></a><a id="CREATE_A_DYNAMIC_VIRTUAL_HARD_DISK"></a>Create a dynamic virtual hard disk</h4>
<p>To create a dynamic virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323659">
<b>CreateVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe CreateDynamicVirtualDisk </b><i>VhdPath</i> <b></b><i>FileSize</i>
<b></b><i>BlockSize</i> <b></b><i>SectorSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>FileSize</i> is the initial maximum size of the virtual hard disk. </li><li><i>BlockSize</i> is the block size of the virtual hard disk, in bytes. </li><li><i>SectorSize</i> is the sector size of the virtual hard disk, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Create_a_differencing_virtual_hard_disk"></a><a id="create_a_differencing_virtual_hard_disk"></a><a id="CREATE_A_DIFFERENCING_VIRTUAL_HARD_DISK"></a>Create a differencing virtual hard disk</h4>
<p>To create a differencing virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323659">
<b>CreateVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe CreateDifferencingVirtualDisk </b><i>VhdPath</i> <b></b><i>ParentPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>ParentPath</i> is the path of the parent virtual hard disk file. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Attach_a_virtual_hard_disk"></a><a id="attach_a_virtual_hard_disk"></a><a id="ATTACH_A_VIRTUAL_HARD_DISK"></a>Attach a virtual hard disk</h4>
<p>To attach a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323692">
<b>AttachVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe AttachVirtualDisk </b><i>VhdPath</i> <b></b><i>ReadOnly</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>ReadOnly</i> is &quot;True&quot; to make the attached drive read only or &quot;False&quot; otherwise.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Detach_a_virtual_hard_disk"></a><a id="detach_a_virtual_hard_disk"></a><a id="DETACH_A_VIRTUAL_HARD_DISK"></a>Detach a virtual hard disk</h4>
<p>To detach a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323696">
<b>DetachVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe DetachVirtualDisk </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Update_information_about_a_virtual_hard_disk"></a><a id="update_information_about_a_virtual_hard_disk"></a><a id="UPDATE_INFORMATION_ABOUT_A_VIRTUAL_HARD_DISK"></a>Update information about a virtual hard disk</h4>
<p>To update information about a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe SetVirtualDiskInformation </b><i>VhdPath</i> <b></b><i>ParentPath</i>
<b></b><i>PhysicalSectorSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>ParentPath</i> is the path of the parent virtual hard disk file. </li><li><i>PhysicalSectorSize</i> is the new physical sector size, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Merge_a_virtual_hard_disk"></a><a id="merge_a_virtual_hard_disk"></a><a id="MERGE_A_VIRTUAL_HARD_DISK"></a>Merge a virtual hard disk</h4>
<p>To merge a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323676">
<b>MergeVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe MergeVirtualDisk </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Compact_a_virtual_hard_disk"></a><a id="compact_a_virtual_hard_disk"></a><a id="COMPACT_A_VIRTUAL_HARD_DISK"></a>Compact a virtual hard disk</h4>
<p>To compact a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Dd323655">
<b>CompactVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe CompactVirtualDisk </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Resize_a_virtual_hard_disk"></a><a id="resize_a_virtual_hard_disk"></a><a id="RESIZE_A_VIRTUAL_HARD_DISK"></a>Resize a virtual hard disk</h4>
<p>To resize a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe ResizeVirtualDisk </b><i>VhdPath</i> <b></b><i>FileSize</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>FileSize</i> is the new maximum size of the virtual hard disk, in bytes. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Mirror_a_virtual_hard_disk"></a><a id="mirror_a_virtual_hard_disk"></a><a id="MIRROR_A_VIRTUAL_HARD_DISK"></a>Mirror a virtual hard disk</h4>
<p>To mirror a virtual hard disk using the <a href="http://msdn.microsoft.com/en-us/library/Hh448678">
<b>MirrorVirtualDisk</b> </a>function, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe MirrorVirtualDisk </b><i>SourcePath</i> <b></b><i>DestinationPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>SourcePath</i> is the path of the source virtual hard disk file. </li><li><i>DestinationPath</i> is the path of the destination virtual hard disk file.
</li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Enumerate_user_metadata_for_a_virtual_hard_disk"></a><a id="enumerate_user_metadata_for_a_virtual_hard_disk"></a><a id="ENUMERATE_USER_METADATA_FOR_A_VIRTUAL_HARD_DISK"></a>Enumerate user metadata for a virtual hard disk</h4>
<p>To enumerate user metadata for a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe EnumerateUserMetaData </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Update_user_metadata_for_a_virtual_hard_disk"></a><a id="update_user_metadata_for_a_virtual_hard_disk"></a><a id="UPDATE_USER_METADATA_FOR_A_VIRTUAL_HARD_DISK"></a>Update user metadata for a virtual hard disk</h4>
<p>To update user metadata for a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe SetUserMetaData </b><i>VhdPath</i> <b></b><i>ID</i> </p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>ID</i> is the new identifier for the virtual hard disk. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Obtain_user_metadata_for_a_virtual_hard_disk"></a><a id="obtain_user_metadata_for_a_virtual_hard_disk"></a><a id="OBTAIN_USER_METADATA_FOR_A_VIRTUAL_HARD_DISK"></a>Obtain user metadata for a virtual hard disk</h4>
<p>To obtain user metadata for a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe GetUserMetaData </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Delete_user_metadata_for_a_virtual_hard_disk"></a><a id="delete_user_metadata_for_a_virtual_hard_disk"></a><a id="DELETE_USER_METADATA_FOR_A_VIRTUAL_HARD_DISK"></a>Delete user metadata for a virtual hard disk</h4>
<p>To obtain user metadata for a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe DeleteUserMetaData </b><i>VhdPath</i> </p>
<p>where <i>VhdPath</i> is the path of the virtual hard disk file.</p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
<h4><a id="Add_a_parent_to_a_virtual_hard_disk"></a><a id="add_a_parent_to_a_virtual_hard_disk"></a><a id="ADD_A_PARENT_TO_A_VIRTUAL_HARD_DISK"></a>Add a parent to a virtual hard disk</h4>
<p>To add a parent to a virtual hard disk, follow these steps.</p>
<ol>
<li>
<p>Enter the debug command line arguments for the project. The usage of this sample is:</p>
<p><b>Storage.exe AddVirtualDiskParent </b><i>VhdPath</i> <b></b><i>ParentPath</i>
</p>
<p>where the parameters are as follows:</p>
<ul>
<li><i>VhdPath</i> is the path of the virtual hard disk file. </li><li><i>ParentPath</i> is the path of the parent virtual hard disk file. </li></ul>
<p></p>
</li><li>
<p>To debug the app and then run it from Visual Studio&nbsp;2010, press F5 or use <b>Debug</b> &gt;
<b>Start Debugging</b>. To run the app without debugging, press Ctrl&#43;F5 or use <b>
Debug</b> &gt; <b>Start Without Debugging</b>.</p>
</li><li>The final result of the operation will be displayed in the console window. </li></ol>
</div>
