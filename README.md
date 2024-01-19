#### updated 1/19/2023 ✂️ 📋 :ramen: v0.9.9.5 release

##### for UE4 games for reference/customization/optimization/learning

##### always testing stuff contact me [smoothschannel](https://twitch.tv/smoothschannel) or [discord](https://discord.gg/tDZT7QSx8m)

##### my config is trying to be quality and perform well for any UE4 game, it might not be perfectly optimal for a specific game

##### make sure your scaling % is set correctly! and match PIP(scope) resolution scaling in games (manually in graphic settings) for PERFORMANCE

##### 2k use 58%(balance) 67%(quality) 70%(custom/TAAU) scaling for PERFORMANCE (DLSS123/TAAU/CAS/FSR123/XeSS)

##### 4k use 33%(ultra performance) 50%(performance/TAAU) scaling for PERFORMANCE (DLSS123/TAAU/CAS/FSR123/XeSS)

---

<details><summary>Open Engine.ini and copy paste under lines in the file</summary>
<p>
press <kbd>⊞ Win+R</kbd> then copy paste
<br>
%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Engine.ini
<br>
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Engine.ini
<br>
%localappdata%/ReadyOrNot/Saved/Config/WindowsNoEditor/Engine.ini
<br>
%localappdata%/SessionGame/Saved/Config/WindowsNoEditor/Engine.ini
<br>
%localappdata%/Chivalry 2/Saved/Config/WindowsNoEditor/Engine.ini
</p>
</details>

```python
[Core.Log]
Global=off;

[Audio]
MaxChannels=32;
CommonAudioPoolSize=0;

[/Script/Engine.Engine]
bSmoothFrameRate=0;
bPauseOnLossOfFocus=0;
bUseFixedFrameRate=0;
DisplayGamma=2.2;

[TextureStreaming]
PoolSizeVRAMPercentage=50;---------------🔵 texturepool cache 🔵 EDITED

[ConsoleVariables]
sg.ResolutionQuality=50;---------------🟡 set correctly
sg.ViewDistanceQuality=0;---------------🔵 EDITED
sg.AntiAliasingQuality=0;---------------🔵 EDITED
sg.ShadowQuality=0;---------------🔵 EDITED
sg.PostProcessQuality=0;---------------🔵 EDITED
sg.TextureQuality=0;---------------🔵 EDITED
sg.EffectsQuality=0;---------------🔵 EDITED
sg.FoliageQuality=0;---------------🔵 EDITED
sg.ShadingQuality=0;---------------🔵 EDITED
r.ScreenPercentage=50;---------------🟡 set correctly
r.SecondaryScreenPercentage.GameViewport=0;---------------🟢 83.33 for PERFORMANCE
r.GTSyncType=0;
r.VSync=0;
rhi.SyncInterval=0;
rhi.SyncSlackMS=0;
r.MSAACount=0;---------------🔵 EDITED
r.DynamicRes.OperationMode=0;
r.SceneRenderTargetResizeMethodForceOverride=0;
r.SceneRenderTargetResizeMethod=0;
r.PostProcessAAQuality=5;---------------🔵 EDITED 🔵 0 for off 1,2 for FXAA 3,4,5,6 for TAA
r.TemporalAA.Algorithm=0;---------------🟢 0 for PERFORMANCE 🔵 1 for Gen5 TAAU
r.TemporalAAFilterSize=0.1;---------------🔵 EDITED 🔵 req Gen5 TAAU
r.TemporalAA.Upsampling=1;---------------🔵 EDITED 🔵 TAAU
r.TemporalAACurrentFrameWeight=0.03;
r.TemporalAASamples=8;
foliage.DensityScale=0.6;---------------🟢 0.6 for PERFORMANCE 🔵 EDITED
foliage.DitheredLOD=1;
foliage.LODDistanceScale=1;
foliage.MinLOD=-1;---------------🟢 1 for PERFORMANCE
foliage.MinInstancesPerOcclusionQuery=1024;---------------🔵 EDITED
foliage.MinimumScreenSize=0.007;---------------🟢 0.007 for PERFORMANCE 🔵 EDITED
foliage.DiscardDataOnLoad=0;
r.AllowSimpleLights=1;---------------🟢 0 for PERFORMANCE
r.ParticleLightQuality=2;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.EmitterSpawnRateScale=1;---------------🟢 0.125,0.5 for PERFORMANCE
r.ParticleMinTimeBetweenTicks=16;
fx.NiagaraAllowRuntimeScalabilityChanges=1;
fx.Niagara.QualityLevel=2;---------------🟢 0 for PERFORMANCE
grass.DensityScale=0.6;---------------🟢 0.6 for PERFORMANCE 🔵 EDITED
grass.DisableDynamicShadows=1;---------------🟢 1 for PERFORMANCE 🔵 EDITED
grass.MaxAsyncTasks=4;
grass.MaxCreatePerFrame=1;
grass.DiscardDataOnLoad=0;
p.AnimDynamics=0;---------------🟢 0 for PERFORMANCE
p.AnimDynamicsWind=1;---------------🟢 0 for PERFORMANCE
p.RigidBodyNode=1;---------------🟢 0 for PERFORMANCE
p.ClothPhysics=1;---------------🟢 0 for PERFORMANCE
r.Tonemapper.Quality=2;---------------🔵 EDITED
r.TonemapperGamma=0;---------------🔵 0 for linear gamma
r.Tonemapper.Sharpen=0;---------------🔵 EDITED
r.MotionBlurQuality=0;---------------🔵 EDITED
r.FastBlurThreshold=7;
r.SceneColorFringeQuality=0;---------------🔵 EDITED
r.FilmGrain=0;
r.EyeAdaptationQuality=1;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.EyeAdaptation.Basic.Compute=1;---------------🟢 1 for PERFORMANCE
r.Upscale.Quality=1;---------------🔵 EDITED
r.Tonemapper.MergeWithUpscale.Mode=1;
r.LensFlarequality=2;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.DepthOfFieldQuality=1;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.DOF.Gather.AccumulatorQuality=0;
r.DOF.Gather.PostfilterMethod=1;---------------🔵 EDITED
r.DOF.Gather.EnableBokehSettings=0;
r.DOF.Gather.RingCount=3;---------------🔵 EDITED
r.DOF.Scatter.ForegroundCompositing=0;---------------🔵 EDITED
r.DOF.Scatter.BackgroundCompositing=0;---------------🔵 EDITED
r.DOF.Scatter.EnableBokehSettings=0;
r.DOF.Scatter.MaxSpriteRatio=0.04;
r.DOF.Recombine.Quality=0;
r.DOF.TemporalAAQuality=0;
r.DOF.Kernel.MaxForegroundRadius=0.006;---------------🔵 EDITED
r.DOF.Kernel.MaxBackgroundRadius=0.006;---------------🔵 EDITED
r.BloomQuality=4;---------------🟢 0 for PERFORMANCE 🔵 EDITED
r.Filter.SizeScale=1;---------------🔵 EDITED
r.LightShaftQuality=1;---------------🟢 0 for PERFORMANCE
r.ViewDistanceScale=1;---------------🟢 0.8 for PERFORMANCE
r.ViewDistanceScale.FieldOfViewAffectsHLOD=0;---------------🟢 0 for PERFORMANCE
r.DetailMode=2;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.RefractionQuality=1;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.SupportAnisotropicMaterials=1;---------------🟢 0 for PERFORMANCE
r.AnisotropicMaterials=1;---------------🟢 0 for PERFORMANCE
r.MaxAnisotropy=8;---------------🟢 0 for PERFORMANCE
r.VT.MaxAnisotropy=8;
r.MaterialQualityLevel=1;---------------🟢 0,2 for PERFORMANCE
r.SupportMaterialLayers=1;---------------🟢 0 for PERFORMANCE
r.SubsurfaceScattering=1;---------------🟢 0 for PERFORMANCE
r.SSS.Quality=0;
r.SSS.SampleSet=0;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.SSS.Checkerboard=1;---------------🟢 1 for PERFORMANCE
r.SSS.HalfRes=1;
r.SSS.Scale=1;
r.SSGI.Enable=0;---------------🟢 0 for PERFORMANCE
r.SSGI.Quality=0;---------------🟢 0,2 for PERFORMANCE 🔵 EDITED 🔵 req SSGI.Enable
r.SceneColorFormat=3;---------------🟢 2,3 for PERFORMANCE
r.HairStrands.Enable=0;---------------🟢 0 for PERFORMANCE
r.TessellationAdaptivePixelsPerTriangle=999999;---------------🟢 999999 for PERFORMANCE 🔵 EDITED
r.LightFunctionQuality=1;---------------🟢 0,1 for PERFORMANCE 🔵 EDITED
r.LightMaxDrawDistanceScale=1;---------------🟢 0.6 for PERFORMANCE
r.MinScreenRadiusForLights=0.03;---------------🟢 0.04,0.06 for PERFORMANCE 🔵 EDITED
r.SkyAtmosphere.AerialPerspectiveLUT.FastApplyOnOpaque=1;
r.SkyAtmosphere.AerialPerspectiveLUT.SampleCountMaxPerSlice=1;---------------🔵 EDITED
r.SkyAtmosphere.AerialPerspectiveLUT.DepthResolution=8;---------------🔵 EDITED
r.SkyAtmosphere.FastSkyLUT=1;
r.SkyAtmosphere.FastSkyLUT.SampleCountMin=4;
r.SkyAtmosphere.FastSkyLUT.SampleCountMax=32;---------------🔵 EDITED
r.SkyAtmosphere.SampleCountMin=4.0
r.SkyAtmosphere.SampleCountMax=32;---------------🔵 EDITED
r.SkyAtmosphere.TransmittanceLUT.UseSmallFormat=0;
r.SkyAtmosphere.TransmittanceLUT.SampleCount=10;
r.SkyAtmosphere.MultiScatteringLUT.SampleCount=15;
r.SkyAtmosphere.MultiScatteringLUT.HighQuality=0;---------------🟢 0 for PERFORMANCE
r.Water.EnableShallowWaterSimulation=0;---------------🟢 0 for PERFORMANCE 🔵 EDITED
r.Water.EnableUnderwaterPostProcess=1;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayer.ShadersSupportDistanceFieldShadow=0;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayer.UnderwaterFog=0;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayer.UnderwaterFogWhenCameraIsAboveWater=0;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayerWater.SupportCloudShadow=0;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayer.Reflection=1;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayer.RefractionDownsampleFactor=2;
r.Water.SingleLayer.SSR=0;---------------🟢 0 for PERFORMANCE
r.Water.SingleLayer.SSRTAA=0;---------------🟢 0 for PERFORMANCE
r.Water.WaterMesh.LODScaleBias=-0.5;---------------🟢 -0.5 for PERFORMANCE 🔵 EDITED
r.Water.WaterMesh.LODCountBias=0;
r.Water.WaterMesh.LODMorphEnabled=0;---------------🟢 0 for PERFORMANCE 🔵 EDITED
r.Water.WaterMesh.TessFactorBias=-1;---------------🟢 -1 for PERFORMANCE 🔵 EDITED
r.Water.SingleLayer.TiledComposite=1;
r.Water.SingleLayer.DepthPrepass=0;
r.SSR.MaxRoughness=0.4;---------------🔵 EDITED
r.SSR.HalfResSceneColor=1;---------------🟢 1 for PERFORMANCE
r.SSR.Quality=2;---------------🟢 0 for PERFORMANCE
r.SSR.Temporal=0;
r.VolumetricFog=1;---------------🟢 0 for PERFORMANCE
r.VolumetricFog.InverseSquaredLightDistanceBiasScale=2;---------------🔵 EDITED
r.VolumetricFog.GridPixelSize=16;
r.VolumetricFog.GridSizeZ=64;
r.VolumetricFog.Jitter=1;
r.VolumetricFog.TemporalReprojection=1;
r.DistanceFields.MaxPerMeshResolution=128;
r.DistanceFields.ParallelAtlasUpdate=1;
r.DistanceFields.ForceMaxAtlasSize=1;
r.DistanceFields.AtlasSizeZ=1024;
r.DistanceFields.AtlasSizeXY=512;
r.GenerateMeshDistanceFields=1;---------------🟢 0 for PERFORMANCE 🔵 1 builds DFS and DFAO mesh
r.DistanceFieldShadowing=1;---------------🟢 0 for PERFORMANCE 🔵 req GenerateMeshDistanceFields
r.DFShadowQuality=1;---------------🟢 0,1,2 for PERFORMANCE 🔵 EDITED 🔵 req DistanceFieldShadowing
r.DFFullResolution=0;---------------🟢 0 for PERFORMANCE
r.DFShadowScatterTileCulling=1;---------------🟢 1 for PERFORMANCE
r.CapsuleShadows=0;---------------🟢 0 for PERFORMANCE 🔵 EDITED
r.ContactShadows=0;---------------🟢 0 for PERFORMANCE 🔵 EDITED
r.AllowLandscapeShadows=1;---------------🟢 0 for PERFORMANCE
r.ShadowQuality=4;---------------🟢 3 for PERFORMANCE 🔵 EDITED
r.Shadow.FilterMethod=0;---------------🟢 0 for PERFORMANCE 🔵 1 for PCSS shadows
r.Shadow.DistanceScale=1;---------------🔵 EDITED
r.Shadow.CSM.MaxCascades=2;---------------🟢 1,2 for PERFORMANCE 🔵 EDITED
r.Shadow.CSM.TransitionScale=1;
r.Shadow.MaxCSMResolution=2048;---------------🟢 1024 for PERFORMANCE
r.Shadow.MaxResolution=1024;---------------🟢 512,1024 for PERFORMANCE 🔵 EDITED
r.Shadow.RadiusThreshold=0.04;
r.Shadow.CachedShadowsCastFromMovablePrimitives=0;---------------🟢 0 for PERFORMANCE 🔵 1 for light cast a shadow
r.Shadow.MaxNumFarShadowCascades=1;---------------🔵 EDITED
r.ParallelShadow=1;---------------🟢 0 for PERFORMANCE
r.ParallelShadowsNonWholeScene=0;---------------🟢 0 for PERFORMANCE
r.ParallelTranslucency=1;
r.ParallelSingleLayerWaterPass=1;
r.TranslucencyLightingVolumeDim=32;---------------🟢 32 for PERFORMANCE 🔵 EDITED
r.TranslucencyVolumeBlur=1;---------------🟢 0 for PERFORMANCE
r.AmbientOcclusionMipLevelFactor=0.6;
r.AmbientOcclusionMaxQuality=-25;---------------🔵 EDITED
r.AmbientOcclusionLevels=2;---------------🟢 0,1 for PERFORMANCE
r.AmbientOcclusionRadiusScale=1;
r.AmbientOcclusionStaticFraction=-1;---------------🟢 0 for PERFORMANCE
r.AmbientOcclusion.Method=0;
r.DistanceFieldAO=0;---------------🟢 0 for PERFORMANCE 🔵 req GenerateMeshDistanceFields
r.AOQuality=0;---------------🟢 0,1 for PERFORMANCE 🔵 req DistanceFieldAO
r.AOGlobalDistanceField=0;---------------🟢 0 for PERFORMANCE 🔵 0 for adaptive method
r.NGX.DLSS.Sharpness=0;
r.NGX.DLSS.AutoExposure=1;
r.NGX.DLSS.Reflections.TemporalAA=0;
r.NGX.DLSS.WaterReflections.TemporalAA=0;
r.HLOD.DistanceOverrideScale=1;
r.HLOD.DistanceOverride=5000;---------------🔵 req HLOD.DistanceOverrideScale
r.HLOD.ForceDisableCastDynamicShadow=0;---------------🟢 1 for PERFORMANCE
r.MipMapLODBias=0;---------------🟢 1 for PERFORMANCE
r.ParticleLODBias=0;
r.LandscapeLODBias=0;
r.SkeletalMeshLODBias=0;
r.Streaming.UseAsyncRequestsForDDC=0;---------------🔵 EDITED
r.Streaming.MipBias=0;
r.Streaming.AmortizeCPUToGPUCopy=0;
r.Streaming.MaxNumTexturesToStreamPerFrame=0;
r.Streaming.Boost=1;
r.Streaming.LimitPoolSizeToVRAM=0;
r.Streaming.UseFixedPoolSize=0;
r.Streaming.PoolSize.Minimum=-1;
r.Streaming.PoolSize.MinimumFreeMemory=-1;
r.Streaming.PoolSize=2048;
r.Streaming.PoolSizeForMeshes=-1;
r.Streaming.HiddenPrimitiveScale=1;---------------🟢 0.5 for PERFORMANCE
r.Streaming.MaxEffectiveScreenSize=0;
r.Streaming.FramesForFullUpdate=12;---------------🔵 EDITED
r.Streaming.NumStaticComponentsProcessedPerFrame=22;---------------🔵 EDITED
r.CompileShadersForDevelopment=0;---------------🔴 DEBUG
r.D3D12.GPUCrashDebuggingMode=0;---------------🔴 DEBUG
r.gpucrash.collectionenable=0;---------------🔴 DEBUG
r.GPUCrashDebugging=0;---------------🔴 DEBUG
r.ShaderDevelopmentMode=0;---------------🔴 DEBUG
r.AmbientOcclusion.Denoiser=0;---------------🔵 EDITED
r.DiffuseIndirect.Denoiser=0;---------------🔵 EDITED
r.Reflections.Denoiser=0;---------------🔵 EDITED
r.Shadow.Denoiser=0;
r.SSR.ExperimentalDenoiser=0;
r.HZBOcclusion=0;
r.AllowOcclusionQueries=1;
r.NumBufferedOcclusionQueries=2;
r.DownsampledOcclusionQueries=1;
r.OneFrameThreadLag=1;
r.FinishCurrentFrame=0;
r.AllowGlobalClipPlane=0;---------------🟢 0 for PERFORMANCE
r.DBuffer=0;---------------🔵 EDITED
r.GBufferFormat=1;
r.ClearCoatNormal=1;---------------🟢 0 for PERFORMANCE
r.IrisNormal=1;---------------🟢 0 for PERFORMANCE
r.DoTiledReflections=1;
r.TiledDeferredShading=1;---------------🟢 0 for PERFORMANCE 🔵 GPU lights
r.DrawRectangleOptimization=1;
r.UniformBufferPooling=1;
r.MeshDrawCommands.AllowOnDemandShaderCreation=1;
```

---

<details><summary>the Scalability.ini way, set @ to what you use in game @0 low @1 med @2 high</summary>
<p>
press <kbd>⊞ Win+R</kbd> then copy paste
<br>
%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Scalability.ini
<br>
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Scalability.ini
<br>
%localappdata%/ReadyOrNot/Saved/Config/WindowsNoEditor/Scalability.ini
<br>
%localappdata%/SessionGame/Saved/Config/WindowsNoEditor/Scalability.ini
<br>
%localappdata%/Chivalry 2/Saved/Config/WindowsNoEditor/Scalability.ini
</p>
</details>

```python
[AntiAliasingQuality@0]
✂️📋

[ViewDistanceQuality@0]
✂️📋

[ShadowQuality@0]
✂️📋

[PostProcessQuality@0]
✂️📋

[TextureQuality@0]
✂️📋

[EffectsQuality@0]
✂️📋

[FoliageQuality@0]
✂️📋

[ShadingQuality@0]
✂️📋
```

---

<details><summary>Open GameUserSettings.ini these commands will overwrite your config so make sure they are correct check for new stuff after updates, good luck</summary>
<p>
press <kbd>⊞ Win+R</kbd> then copy paste
<br>
%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/GameUserSettings.ini
<br>
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/GameUserSettings.ini
<br>
%localappdata%/ReadyOrNot/Saved/Config/WindowsNoEditor/GameUserSettings.ini
<br>
%localappdata%/SessionGame/Saved/Config/WindowsNoEditor/GameUserSettings.ini
<br>
%localappdata%/Chivalry 2/Saved/Config/WindowsNoEditor/GameUserSettings.ini
</p>
</details>

```python
AmbientOcclusion=(Value=?);
AntiAliasingMode=(Value=?);
AudioQualityLevel=?;
bBounceLightEnabled=?;
bConsoleEnabled=?;
bDepthOfField=?;
bFlashlightShadowsEnabled=?;
bFrameLimitEnabled=?;
bMotionBlur=?;
bRTXAmbientOcclusionEnabled=?;
bRTXEnabled=?;
bRTXReflectionsEnabled=?;
bRTXShadowsEnabled=?;
bTelemetryEnabled=?;
bUseDynamicResolution=?;
bUseVSync=?;
ContactShadows=(Value=?);
ContactShadows=?;
DetailMode=(Value=?);
DFAO=?;
DistanceFieldShadows=?;
DlssQualitySetting=?;
DoubleKeyPressTime=?;
FoliageMinLOD=(Value=?);
FrameRateLimit=?;
FullscreenMode=?;
Gamma=?;
GlobalSensitivity=?;
GraphicsPresetIndex=?;
GraphicsQuality=?;
HDRDisplayOutputNits=?;
HZBOcclusion=(Value=?);
LastSavedAAQuality=?;
LastSavedAASamples=?;
MaxAnisotropy=(Value=?);
MaxAnisotropy=?;
MaxFPS=?;
MenuFrameRateLimit=?;
OceanQuality=(Value=?);
OverrideOptions=(("r.command",(Value=?,bModified=True)),("r.command",(Value=?,bModified=True)));
PostFX_Saturation=?;
PostFX_Sharpness=?;
ResolutionScaleModifier=?;
ScreenPercentage=(Value=?);
SkeletalMeshLODBias=(Value=?);
TAASampleStorage=?;
TemporalAASamples=(Value=?);
Tessellation=(Value=?);
TessellationMode=(Value=?);
TextureStreamPoolSizeStorage=(Value=?);
WakeSim=(Value=?)

[ScalabilityGroups]
sg.ResolutionQuality=50;---------------🟡 set correctly
sg.ViewDistanceQuality=2;---------------🟢 0 for PERFORMANCE
sg.AntiAliasingQuality=2;---------------🟢 0 for PERFORMANCE
sg.ShadowQuality=2;---------------🟢 0 for PERFORMANCE
sg.PostProcessQuality=2;---------------🟢 0 for PERFORMANCE
sg.TextureQuality=2;---------------🟢 0 for PERFORMANCE
sg.EffectsQuality=2;---------------🟢 0 for PERFORMANCE
sg.FoliageQuality=2;---------------🟢 0 for PERFORMANCE
```

---

<details><summary>Open Input.ini and edit input commands or add them</summary>
<p>
press <kbd>⊞ Win+R</kbd> then copy paste
<br>
%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Input.ini
<br>
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Input.ini
<br>
%localappdata%/ReadyOrNot/Saved/Config/WindowsNoEditor/Input.ini
<br>
%localappdata%/SessionGame/Saved/Config/WindowsNoEditor/Input.ini
<br>
%localappdata%/Chivalry 2/Saved/Config/WindowsNoEditor/Input.ini
</p>
</details>

```python
[/Script/Engine.InputSettings]
bAltEnterTogglesFullscreen=1;
bF11TogglesFullscreen=0; 
bEnableMouseSmoothing=0;
bViewAccelerationEnabled=0;
InitialButtonRepeatDelay=0.15;---------------🔵 EDITED
ButtonRepeatDelay=0.1;
DoubleClickTime=0.2;---------------🔵 EDITED
```

---

<details><summary>Open DeviceProfiles.ini for textures lods, should lower gpu utilization, most MaxLODSize in games are 4096. Feel free to just skip this and use devs defaults</summary>
<p>
press <kbd>⊞ Win+R</kbd> then copy paste
<br>
%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
<br>
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
<br>
%localappdata%/ReadyOrNot/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
<br>
%localappdata%/SessionGame/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
<br>
%localappdata%/Chivalry 2/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
</p>
</details>

```python
[/Script/Engine.TextureLODSettings]
TextureLODGroups=(Group=TEXTUREGROUP_World,                 MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WorldNormalMap,        MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WorldSpecular,         MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Character,             MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_CharacterNormalMap,    MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_CharacterSpecular,     MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Weapon,                MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WeaponNormalMap,       MinLODSize=128,  MaxLODSize=512,  OptionalMaxLODSize=256,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WeaponSpecular,        MinLODSize=128,  MaxLODSize=512,  OptionalMaxLODSize=256,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Vehicle,               MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_VehicleNormalMap,      MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_VehicleSpecular,       MinLODSize=256,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Cinematic,             MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Effects,               MinLODSize=128,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=linear, MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_EffectsNotFiltered,    MinLODSize=128,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Skybox,                MinLODSize=2048, MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_UI,                    MinLODSize=2048, MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Lightmap,              MinLODSize=32,   MaxLODSize=32,                            LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
TextureLODGroups=(Group=TEXTUREGROUP_Shadowmap,             MinLODSize=32,   MaxLODSize=32,                            LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
TextureLODGroups=(Group=TEXTUREGROUP_RenderTarget,          MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_MobileFlattened,       MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_ProcBuilding_Face,     MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_ProcBuilding_LightMap, MinLODSize=32,   MaxLODSize=32,                            LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
TextureLODGroups=(Group=TEXTUREGROUP_ColorLookupTable,      MinLODSize=2048, MaxLODSize=2048,                          LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
TextureLODGroups=(Group=TEXTUREGROUP_Terrain_Heightmap,     MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Terrain_Weightmap,     MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Bokeh,                 MinLODSize=256,  MaxLODSize=256,                           LODBias=0, MinMagFilter=linear, MipFilter=linear, MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
TextureLODGroups=(Group=TEXTUREGROUP_IESLightProfile,       MinLODSize=256,  MaxLODSize=2048, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Pixels2D,              MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=point,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_HierarchicalLOD,       MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_8BitData,                                                                         LODBias=0, MinMagFilter=point,  MipFilter=point,  MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
TextureLODGroups=(Group=TEXTUREGROUP_16BitData,                                                                        LODBias=0, MinMagFilter=point,  MipFilter=point,  MipGenSettings=TMGS_NoMipmaps,     NumStreamedMips=0);
```

---

#### Open NVIDIA Control Panel

##### 1. 3D settings -> adjust image settings with preview -> use my preference emphasizing performance apply.

##### 2. click on use the advanced 3D image settings and apply then click "take me there"

##### 3. Anisotropic filtering:  set Application-controlled (you can force the setting in here if you can't notice it working in certain games)

##### 4. Low latency mode (Only works with dx11 and lower api):

###### Off and ~85% gpu usage for multiple frame buffers sacrificing latency (cap fps til gpu usage is ~85%) (for visual fluidity of frames)

###### On forces 1 frame buffer (for lower latency than off) (for visual fluidity of frames and less latency)

###### Ultra and high gpu usage for lowest latency

###### Nvidia relfex is in-game and dx12 only and you should use it just like Ultra low latency mode with high gpu usage

##### 5. Power management mode:  prefer max performance  (this is the "+ boost" in reflex + boost)

##### 6. Preferred refresh rate:  Highest available

##### 7. Texture filtering - anisotropic sample optimization:  on  (off will look better if this even works in your game)

##### 8. Texture filtering - negative LOD bias:  allow (allows a negative bias) clamp (0 mipmap bias) test yourself devs usually set slight negative clamps, also negative with DLSS/FSR2 upscaling

##### 9. Texture filtering quality:  high performance

##### 10. Texture filtering - trilinear optimization:  on

##### 11. Vertical sync:  Off

##### 12. Display -> Adjust desktop size and position -> set Perform scaling on: Display

#### Turn on Message-signaled interrupts (MSIs) (better than line based interrupt method)

###### NVCleanstall enabling it in advanced settings before installing or

#### Manually enable Message-signaled interrupts (MSIs)

###### win + r type cmd then press control+shift+enter (starts as admin) then add key. NVcleaninstall gives you more MSIs options. Newest drivers auto do this on 40 series cards, i wonder if its default or set to high.

```python
reg add "HKLM\SYSTEM\ControlSet001\Enum\PCI\VEN_10DE&DEV_1E84&SUBSYS_139E10DE&REV_A1\4&3aaa5e18&0&0008\Device Parameters\Interrupt Management\MessageSignaledInterruptProperties" /v MSISupported /t REG_DWORD /d 1 /f
```

###### restart

###### in device manager/view/resources by connection/GPU name should have a negative number in parentheses if MSIs is enabled

#### Disable HPET (High Precision event timer) in device manager/system devices and/or in your bios to get lower latency and more fps
