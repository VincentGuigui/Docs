Reconstruction Class  
====================  

Reconstruction encapsulates reconstruction volume creation updating and meshing functions. <span id="syntaxSection"></span>

Syntax  
======  

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><pre><code>public ref class Reconstruction sealed</code></pre></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><pre><code>public sealed class Reconstruction</code></pre></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">JavaScript</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><pre><code>var reconstruction = Microsoft.Kinect.Fusion.Reconstruction;</code></pre></td>
</tr>
</tbody>
</table>

<span id="classMembersSection"></span>

Members  
=======  

**Reconstruction** has the following members.  

<span id="publicconstructorsSection"></span>

Constructors  
============  

<table>
<colgroup>
<col width="30%" />
<col width="60%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Constructor.md">Reconstruction</a></td>
<td align="left">Overloaded. Initializes a new instance of the <a href="">Reconstruction</a> class.</td>
</tr>
</tbody>
</table>

<span id="publicmethodsSection"></span>

Methods  
=======  

<table>
<colgroup>
<col width="30%" />
<col width="60%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/AlignDepthFloatFrameToReco.md">AlignDepthFloatFrameToReconstruction</a></td>
<td align="left">Aligns a depth float image to the reconstruction volume to calculate the new camera pose.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/AlignPointClouds_Method.md">AlignPointClouds</a></td>
<td align="left">Aligns two sets of overlapping oriented point clouds and calculates the camera's relative pose.</td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/CalculateMesh_Method.md">CalculateMesh</a></td>
<td align="left">Exports a polygon mesh of the zero-crossing dense surfaces from the reconstruction volume with per-vertex color.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/CalculatePointCloud_Method.md">CalculatePointCloud</a></td>
<td align="left">Calculates a point cloud by raycasting into the reconstruction volume, returning the point cloud containing 3D points and normals of the zero-crossing dense surface at every visible pixel in the image from the specified camera pose and color visualization image.</td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/CalculatePointCloudAndDepth.md">CalculatePointCloudAndDepth</a></td>
<td align="left">Calculates a point cloud by raycasting into the reconstruction volume, returning the point cloud containing 3D points and normals of the zero-crossing dense surface at every visible pixel in the image from the specified camera pose, color visualization image, and the depth to the surface.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/DepthToDepthFloatFrame.md">DepthToDepthFloatFrame</a></td>
<td align="left">Converts the specified buffer of Kinect depth pixels to a <a href="DepthFloatFrame_Class.md">DepthFloatFrame</a> object.</td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/ExportVolumeBlock_Method.md">ExportVolumeBlock</a></td>
<td align="left">Exports a part or all of the reconstruction volume as a buffer of shorts.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/GetCurrentWorldToCameraTra.md">GetCurrentWorldToCameraTransform</a></td>
<td align="left">Retrieves the current internal world-to-camera transform (camera view pose).</td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/GetCurrentWorldToVolumeTra.md">GetCurrentWorldToVolumeTransform</a></td>
<td align="left">Get current internal world-to-volume transform.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/ImportVolumeBlock_Method.md">ImportVolumeBlock</a></td>
<td align="left">Imports a reconstruction volume as a short array.</td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/IntegrateFrame_Method.md">IntegrateFrame</a></td>
<td align="left">Integrates depth float data into the reconstruction volume from the passed camera pose.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/ProcessFrame_Method.md">ProcessFrame</a></td>
<td align="left">A high-level function to process a depth frame through the Kinect Fusion pipeline.</td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/ResetReconstruction_Method.md">ResetReconstruction</a></td>
<td align="left">Clear the reconstruction volume, and set a world-to-camera transform (camera view pose) and a world-to-volume transform.</td>
</tr>
<tr class="even">
<td align="left"><a href="Reconstruction_Class/Methods/SetAlignDepthFloatToRecons.md">SetAlignDepthFloatToReconstructionReferenceFrame</a></td>
<td align="left">Sets a reference depth frame that is used internally to help with tracking when calling the <a href="Reconstruction_Class/Methods/AlignDepthFloatFrameToReco.md">AlignDepthFloatFrameToReconstruction</a> method to calculate a new camera pose.  
<div class="alert">
<table>
<thead>
<tr class="header">
<th align="left"><img src="../../../../resources/note.gif" />Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">You should call this method only if you are not using the default tracking behavior of Kinect Fusion.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="odd">
<td align="left"><a href="Reconstruction_Class/Methods/SmoothDepthFloatFrame_Method.md">SmoothDepthFloatFrame</a></td>
<td align="left">Spatially smoothes a depth float image frame using edge-preserving filtering.</td>
</tr>
</tbody>
</table>

<span id="remarks"></span>

Remarks  
=======  

| ![](../../../../resources/note.gif)Important                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| When passing frames with a resolution that differs from that of the frames that were previously passed to the reconstruction volume, call the [ResetReconstruction](Reconstruction_Class/Methods/ResetReconstruction_Method.md) method before processing the frames with the new resolution. Failure to reset the volume can result in camera tracking failure and erroneous volume data. |

<span id="requirements"></span>

Requirements  
============  

**Namespace:**Microsoft.Kinect.Fusion  
**Metadata:**microsoft.kinect.fusion.winmd  

<span id="ID4EAB"></span>

See also  
========  

<span id="ID4ECB"></span>
#### Reference  

[Microsoft.Kinect.Fusion Namespace](../Kinect.Fusion.md)  



<!--Please do not edit the data in the comment block below.-->
<!--
TOCTitle : Reconstruction Class
RLTitle : Reconstruction Class
KeywordK : Reconstruction class, about
HelpPriority : 2
TopicType : apiref
KeywordF : Microsoft.Kinect.Fusion.Reconstruction
KeywordF : Reconstruction
KeywordF : Microsoft.Kinect.Fusion.Reconstruction
KeywordA : T:Microsoft.Kinect.Fusion.Reconstruction
AssetID : T:Microsoft.Kinect.Fusion.Reconstruction
Locale : en-us
CommunityContent : 1
APIType : Managed
APILocation : microsoft.kinect.fusion.winmd
APIName : Microsoft.Kinect.Fusion.Reconstruction
TargetOS : Windows
TopicType : kbSyntax
DevLang : VB
DevLang : CSharp
DevLang : JavaScript
DevLang : C++
DocSet : K4Wv2
ProjType : K4Wv2Proj
Technology : Kinect for Windows
Product : Kinect for Windows SDK v2
productversion : 20
-->
