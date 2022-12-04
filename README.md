
#### updated 12/4/2022~ :ramen:

###### for UE4 games for reference/customization/optimization/learning

###### always testing stuff contact me [smoothschannel](https://twitch.tv/smoothschannel) or [discord](https://discord.gg/vB8f4fZ7EH)

###### my config is trying to be quality and perform well for any UE4 game, it might not be perfectly optimal for a specific game

###### def is pretty much reference to high scalablity group

###### Use Nvidia Image Scaling and turn down in game res for more fps

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
MaxChannels=64;------def 0------changed to 64*------64 for PERFORMANCE
CommonAudioPoolSize=0;------def 0
UnfocusedVolumeMultiplier=1;

[/Script/Engine.Engine]
bSmoothFrameRate=0;
bPauseOnLossOfFocus=0;
bUseFixedFrameRate=0;
DisplayGamma=2.2;

[TextureStreaming]
PoolSizeVRAMPercentage=64;------def 70------TEXTUREPOOL CACHE------changed

[ConsoleVariables]
r.DefaultFeature.AntiAliasing=2;------1 FXAA 2 TAA 3 MSAA 0 OFF------changed
r.PostProcessAAQuality=5;------1 or 2 FXAA 3 or 4 5 6 TAA 0 OFF------changed
r.ScreenPercentage=100;------def 100------TAAU INPUT RESOLUTION
r.SecondaryScreenPercentage.GameViewport=0;------def 0------83.33 for PERFORMANCE
r.TemporalAA.Algorithm=0;------def 0
r.TemporalAA.AllowDownsampling=1;------def 1
r.TemporalAA.HistoryScreenPercentage=100;------def 100
r.TemporalAA.R11G11B10History=0;------def 0------EXPERIMENTAL
r.TemporalAA.Upsampling=0;------def 0
r.TemporalAA.Upscaler=1;------def 1
r.TemporalAACatmullRom=0;------def 0
r.TemporalAACurrentFrameWeight=0.2;------def 0.1------changed
r.TemporalAAFilterSize=1;------def 1
r.TemporalAAPauseCorrect=1;------def 1
r.TemporalAASamples=4;------def 8------changed
r.TemporalAAUpsampleFiltered=1;------def 1
au.RenderThreadPriority=0;------def 0
AudioThread.BatchAsyncBatchSize=128;------def 128
AudioThread.EnableBatchProcessing=1;------def 1
Compat.UseDXT5NormalMaps=0;------def 0
foliage.DensityScale=0.6;------def 0.8------0.6 for PERFORMANCE------changed
foliage.DitheredLOD=1;------def 1
foliage.LODDistanceScale=1;------def 1
foliage.MinimumScreenSize=0.0001;------def 0.0001
foliage.MinLOD=1;------def 0------1 for PERFORMANCE------changed
foliage.MinVertsToSplitNode=8192;------def 8192
foliage.OverestimateLOD=0;------def 0
FX.AllowAsyncTick=1;------def 1
FX.AllowGPUParticles=1;------def 1
FX.AllowGPUSorting=1;------def 1
FX.BatchAsync=0;------def 0
FX.BatchAsyncBatchSize=32;------def 32
FX.FXAllowParticleMeshLODs=0;------def 0
FX.ParticleCollisionIgnoreInvisibleTime=0.1;------def 0.1
FX.ParticleManagerAsyncBatchSize=8;------def 8
FX.ParticleSystemPool.CleanTime=30;------def 30
FX.ParticleSystemPool.Enable=1------def 1
FX.ParticleSystemPool.KillUnusedTime=180;------def 180
FX.QualityLevelSpawnRateScaleReferenceLevel=2;------def 2------0 for PERFORMANCE
grass.DensityScale=0.6;------def 1------0.6 for PERFORMANCE------changed
grass.DisableDynamicShadows=0;------def 0------1 for PERFORMANCE
grass.TickInterval=10;------def 1------10 for PERFORMANCE------changed
p.AllowCachedOverlaps=1;------def 1
p.AnimDynamics=1;------def 1------0 for PERFORMANCE
p.AnimDynamicsLODThreshold=-1;------def -1
p.AnimDynamicsRestrictLOD=-1;------def -1
p.AnimDynamicsWind=1;------def 1
p.BatchPhysXTasksSize=3;------def 3
p.ClothPhysics=1;------def 1------0 for PERFORMANCE
p.RigidBodyLODThreshold=-1;------def -1
p.RigidBodyNode=1;------def 1
r.AllowDownsampledStandardTranslucency=0;------def 0
r.AllowGlobalClipPlane=0;------def 0
r.AllowHDR=0;------def 0
r.AllowLandscapeShadows=1;------def 1------0 for PERFORMANCE
r.AllowPointLightCubemapShadows=1;------def 1------0 for PERFORMANCE
r.AllowSimpleLights=1;------def 1------0 for PERFORMANCE
r.AlsoUseSphereForFrustumCull=0;------def 0------1 for PERFORMANCE
r.AmbientOcclusion.AsyncComputeBudget=1;------def 1
r.AmbientOcclusion.Compute.Smooth=1;------def 1
r.AmbientOcclusion.Compute=0;------def 0------1 for PERFORMANCE
r.AmbientOcclusionLevels=1;------def 3------0 for PERFORMANCE------changed
r.AmbientOcclusionMaxQuality=100;------def 100
r.AmbientOcclusionMipLevelFactor=1;------def 0.6------changed
r.AmbientOcclusionRadiusScale=0.01;------def 1------changed
r.AmbientOcclusionStaticFraction=-1;------def -1
r.AnisotropicMaterials=0;------def 1------0 for PERFORMANCE------changed
r.AOApplyToStaticIndirect=0;------def 0
r.AOComputeShaderNormalCalculation=0;------def 0
r.AOGlobalDFResolution=128;------def 128
r.AOHeightfieldOcclusion=0;------def 0
r.AOOverwriteSceneColor=0;------def 0
r.AOQuality=1;------def 1
r.AOSampleSet=1;------def 1
r.AOViewFadeDistanceScale=0.7;------def 0.7
r.Bloom.Cross=0;------def 0-------Anamorphic 0.7777
r.Bloom.HalfResolutionFFT=0;------def 0------EXPERIMENTAL
r.BloomQuality=3;------def 4------changed
r.CapsuleShadows=0;------def 1------0 for PERFORMANCE------changed
r.CapsuleShadowsFullResolution=0;------def 0
r.chaos.ReflectionCaptureStaticSceneOnly=1;------def 1
r.ClearCoatNormal=0;------def 0
r.CompileShadersForDevelopment=0;------def 1------0 for PERFORMANCE------changed
r.ContactShadows.NonShadowCastingIntensity=0;------def 0
r.ContactShadows=1;------def 1------0 for PERFORMANCE
r.CreateShadersOnLoad=1;------def 0------changed
r.D3D11.Depth24Bit=0;------def 0------1 for PERFORMANCE
r.D3D12.Depth24Bit=0;------def 0------1 for PERFORMANCE
r.DBuffer=1;------def 1------0 for PERFORMANCE
r.Decal.FadeDurationScale=0.5;------def 1------0.5 for PERFORMANCE------changed
r.Decal.FadeScreenSizeMult=1;------def 1
r.Decal.StencilSizeThreshold=0;------def 0.1------changed
r.DefaultBackBufferPixelFormat=4;------def 4
r.DefaultFeature.AmbientOcclusion=1;------def 1
r.DefaultFeature.AmbientOcclusionStaticFraction=1;------def 1------0 for PERFORMANCE
r.DefaultFeature.Bloom=1;------def 1
r.DefaultFeature.LensFlare=1;------def 1
r.DefaultFeature.LightUnits=1;------def 1
r.DefaultFeature.MotionBlur=0;------def 0
r.DeferSkeletalDynamicDataUpdateUntilGDME=0;------def 0------EXPERIMENTAL
r.DeferUniformExpressionCaching=1;------def 1
r.DepthOfFieldQuality=0;------def 2------0 for PERFORMANCE------changed
r.DetailMode=1;------def 1------0 for PERFORMANCE
r.DFDistanceScale=1;------def 1
r.DFFullResolution=0;------def 0
r.DFShadowQuality=2;------def 3------1 or 2 for PERFORMANCE------changed
r.DFShadowScatterTileCulling=1;------def 1
r.DFTwoSidedMeshDistanceBias=5;------def 4------changed
r.DiscardUnusedQuality=0;------def 0
r.DistanceFieldAO=0;------def 0
r.DistanceFieldShadowing=1;------def 1------0 for PERFORMANCE
r.DoInitViewsLightingAfterPrepass=0;------def 0------EXPERIMENTAL
r.DoLazyStaticMeshUpdate=0;------def 0------EXPERIMENTAL
r.DoPrepareDistanceFieldSceneAfterRHIFlush=1;------def 1
r.DoTiledReflections=1;------def 1------0 for PERFORMANCE
r.Downsample.Quality=1;------def 1
r.DrawRectangleOptimization=1;------def 1
r.EarlyZPass=2;------def 2
r.EarlyZPassMovable=1;------def 1
r.EarlyZPassOnlyMaterialMasking=1;------def 1
r.Emitter.FastPoolEnable=1;------def 0------changed
r.Emitter.FastPoolMaxFreeSize=3072000;------def 2097152------changed
r.EmitterSpawnRateScale=0.5;------def 1------0.125 for PERFORMANCE------changed
r.EnableAsyncComputeTranslucencyLightingVolumeClear=1;------def 1
r.FastBlurThreshold=3;------def 3
r.Filter.SizeScale=0.8;------def 0.8
r.FinishCurrentFrame=0;------def 0
r.ForceSceneHasDecals=0;------def 0
r.FreeSkeletalMeshBuffers=0;------def 0
r.FullScreenMode=0;------def 0------0 for PERFORMANCE
r.GBufferFormat=0;------def 1------0 for PERFORMANCE------changed
r.GenerateLandscapeGIData=1;------def 1
r.GenerateMeshDistanceFields=1;------1 for DFSHADOWS and or DFAO------0 for PERFORMANCE
r.GPUCrash.CollectionEnable=0;------def 1------changed
r.GPUCrashDebugging=0;------def 0
r.GPUSkin.Limit2BoneInfluences=0;------def 0
r.GTSyncType=0;------def 0
r.HairStrands.SkyLighting=1;------def 1
r.HDR.EnableHDROutput=0;------def 0
r.HeightFieldShadowing=1;------def 0------changed
r.HFShadowQuality=1;------def 2------0 or 1 for PERFORMANCE------changed
r.HighQualityLightMaps=1;------def 1
r.HZBOcclusion=0;------def 0
r.IrisNormal=0;------def 0
r.LandscapeLOD0DistributionScale=1;------def 1
r.LandscapeLODBias=0;------def 0------1 for PERFORMANCE
r.LandscapeLODDistributionScale=1;------def 1
r.LensFlareQuality=2;------def 2------0 for PERFORMANCE
r.LightFunctionQuality=1;------def 1
r.LightMaxDrawDistanceScale=1;------def 1------0.6 for PERFORMANCE
r.LightShaftAllowTAA=1;------def 1
r.LightShaftQuality=0;------def 1------0 for PERFORMANCE------changed
r.LightShaftRenderToSeparateTranslucency=0;------def 0
r.MaterialQualityLevel=1;------def 1------0 for PERFORMANCE
r.MaxAnisotropy=8;------def 4------changed
r.MaxQualityMode=0;------def 0
r.MinRoughnessOverride=0;------def 0
r.MinScreenRadiusForCSMDepth=0.01;------def 0.01
r.MinScreenRadiusForDepthPrepass=0.03;------def 0.03
r.MinScreenRadiusForLights=0.03;------def 0.03------0.06 for PERFORMANCE
r.MinTimeBetweenTicks=12;------def 8 or 16------changed
r.MipMapLODBias=1;------def 0------2 for PERFORMANCE------changed
r.MorphTarget.Mode=1;------def 1
r.MotionBlurQuality=0;------def 3------changed
r.MSAACount=0;------def 4------changed
r.NormalMapsForStaticLighting=1;------def 1------0 for PERFORMANCE
r.NumBufferedOcclusionQueries=1;------def 1
r.OneFrameThreadLag=1;------def 1
r.ParticleLightQuality=1;------def 1------0 for PERFORMANCE
r.ParticleLODBias=0;------def 0
r.ParticleMinTimeBetweenTicks=12;------def 8 or 16------changed
r.PostProcessAllowBlendModes=1;------def 1
r.ReflectionCaptureSupersampleFactor=1;------def 1
r.ReflectionEnvironment=1;------def 1------0 for PERFORMANCE
r.ReflectionEnvironmentLightmapMixLargestWeight=10000;------def 10000
r.RefractionQuality=1;------def 2------0 for PERFORMANCE------changed
r.RenderTargetPool.AllowMultipleAliasingDiscardsPerFrame=0;------def 0
r.RenderTargetPool.TransientAliasingMode=2;------def 2
r.RenderTargetPoolMin=400;------def 400
r.SceneColorFormat=3;------def 3
r.SceneColorFringe.Max=-1;------def -1
r.SceneColorFringeQuality=0;------def 1------changed
r.SceneRenderTargetResizeMethod=0;------def 0
r.SceneRenderTargetResizeMethodForceOverride=0;------def 0
r.SeparateTranslucency=0;------def 1------0 for PERFORMANCE------changed
r.ShaderDevelopmentMode=0;------def 0
r.Shaders.FastMath=1;------def 1
r.Shaders.Optimize=1;------def 1
r.Shadow.CachedShadowsCastFromMovablePrimitives=1;------def 1------0 for PERFORMANCE
r.Shadow.CacheWholeSceneShadows=1;------def 1
r.Shadow.CacheWPOPrimitives=0;------def 0
r.Shadow.CSM.MaxCascades=4;------def 3------1 or 2 for PERFORMANCE------changed
r.Shadow.CSM.TransitionScale=0.8;------def 0.8
r.Shadow.CSMDepthBias=10;------def 10
r.Shadow.DistanceScale=0.7;------def 0.85------changed
r.Shadow.FilterMethod=0;------def 0
r.Shadow.MaxCSMResolution=1024;------def 2048------512 or 1024 for PERFORMANCE------changed
r.Shadow.MaxNumFarShadowCascades=4;------def 10------0 for PERFORMANCE------changed
r.Shadow.MaxNumPointShadowCacheUpdatesPerFrame=2;------def -1------2 for PERFORMANCE------changed
r.Shadow.MaxNumSpotShadowCacheUpdatesPerFrame=4;------def -1------4 for PERFORMANCE------changed
r.Shadow.MaxResolution=1024;------def 2048------1024 for PERFORMANCE------changed
r.Shadow.OcclusionCullCascadedShadowMaps=0;------def 0
r.Shadow.PointLightDepthBias=0.02;------def 0.02
r.Shadow.PointLightSlopeScaleDepthBias=3;------def 3
r.Shadow.RadiusThreshold=0.02;------def 0.04------0.06 for PERFORMANCE------changed
r.Shadow.SpotLightTransitionScale=60;------def 60
r.Shadow.TransitionScale=60;------def 60
r.ShadowQuality=3;------def 4------3 for PERFORMANCE------changed
r.SkeletalMeshLODBias=0;------def 0------2 or 1 for PERFORMANCE
r.SkeletalMeshLODRadiusScale=1;------def 1
r.SkinCache.SceneMemoryLimitInMB=128;------def 128
r.SkyAtmosphere.MultiScatteringLUT.HighQuality=0;------def 0
r.SkyAtmosphere.TransmittanceLUT.UseSmallFormat=0;------def 0
r.SkyAtmosphere=1;------def 1
r.SkyLightingQuality=1;------def 1
r.SkylightIntensityMultiplier=1;------def 1
r.SSGI.Quality=0;------def 2------0 for PERFORMANCE------changed
r.SSR.HalfResSceneColor=1;------def 1
r.SSR.MaxRoughness=-1;------def -1
r.SSR.Quality=0;------def 2------0 for PERFORMANCE------changed
r.SSR.Temporal=0;------def 0
r.SSS.Checkerboard=1;------def 2------changed
r.SSS.HalfRes=1;------def 1
r.SSS.Quality=0;------def -1------0 for PERFORMANCE------changed
r.StaticMeshLODDistanceScale=1;------def 1
r.Streaming.AmortizeCPUToGPUCopy=1;------def 0------1 for PERFORMANCE------changed
r.Streaming.FullyLoadUsedTextures=0;------def 0
r.Streaming.LimitPoolSizeToVRAM=1;------def 1
r.Streaming.MaxNumTexturesToStreamPerFrame=5;------def 0------5 for PERFORMANCE------changed
r.Streaming.MaxTempMemoryAllowed=50;------def 50
r.Streaming.MinLevelRenderAssetScreenSize=100;------def 100
r.Streaming.MipBias=0;------def 0------1 for PERFORMANCE
r.Streaming.MipCalculationEnablePerLevelList=1;------def 1
r.Streaming.PoolSize.VRAMPercentageClamp=1024;------def 1024
r.Streaming.PoolSize=800;------def 800
r.Streaming.PoolSizeForMeshes=-1;------def -1
r.Streaming.UseFixedPoolSize=0;------def 0
r.Streaming.UsePerTextureBias=1;------def 1
r.SupportAnisotropicMaterials=1;------def 1------0 for PERFORMANCE
r.SupportMaterialLayers=1;------def 1------0 for PERFORMANCE
r.SupportSkyAtmosphere=1;------def 1
r.SupportSkyAtmosphereAffectsHeightFog=1;------def 1
r.TessellationAdaptivePixelsPerTriangle=9999999;------def 48------9999999 for PERFORMANCE------changed
r.TextureStreaming=1;------def 1
r.TiledDeferredShading.MinimumCount=80;------default 80
r.TiledDeferredShading=1;------def 1------0 for PERFORMANCE
r.Tonemapper.EmulateHDR=0;------def 0
r.Tonemapper.GrainQuantization=1;------def 1------0 for PERFORMANCE
r.Tonemapper.MergeWithUpscale.Mode=0;------def 0
r.Tonemapper.MergeWithUpscale.Threshold=0.49;------def 0.49
r.Tonemapper.Quality=3;------def 5------0 for PERFORMANCE------changed
r.Tonemapper.Sharpen=0;------def 0
r.TonemapperGamma=0;------def 0
r.TranslucencyLightingVolume=1;------def 1------0 for PERFORMANCE
r.TranslucencyLightingVolumeDim=32;------def 48------32 for PERFORMANCE------changed
r.UITextureLODBias=0;------def 0
r.UniformBufferPooling=1;------def 1
r.Upscale.Quality=2;------def 2
r.Upscale.Softness=1;------def 1
r.UseClusteredDeferredShading=0;------def 0
r.UseFastIntersect=1;------def 1
r.UseParallelGetDynamicMeshElementsTasks=0;------def 0
r.ViewDistanceScale.ApplySecondaryScale=0;------def 0
r.ViewDistanceScale.SecondaryScale=1;------def 1
r.ViewDistanceScale=0.8;------def 1------0.8 for PERFORMANCE------changed
r.VirtualTexture=0;------def 1------changed
r.VirtualTexturedLightmaps=0;------def 0
r.VirtualTextureReducedMemory=0;------def 0
r.VirtualTextures=0;------def 1------changed
r.VolumetricCloud.ShadowMap=0;------def 1------0 for PERFORMANCE------changed
r.VolumetricCloud.SkyAO=0;------def 1------0 for PERFORMANCE------changed
r.VolumetricCloud=0;------def 1------0 for PERFORMANCE------changed
r.VolumetricFog.GridPixelSize=32;------def 16------changed
r.VolumetricFog.HistoryMissSupersampleCount=1;------def 4------0 for PERFORMANCE------changed
r.VolumetricFog.InjectShadowedLightsSeparately=0;------def 1------0 for PERFORMANCE------changed
r.VolumetricFog=0;------def 1------0 for PERFORMANCE------changed
r.VSync=0;------def 0
r.VT.MaxAnisotropy=8;------def 8
r.Vulkan.Depth24Bit=0;------def 0------1 for PERFORMANCE
r.Water.EnableShallowWaterSimulation=1;------def 1------0 for PERFORMANCE
r.Water.EnableUnderwaterPostProcess=1;------def 1------0 for PERFORMANCE
r.Water.ShallowWaterRenderTargetSize=512;------def 1024------changed
r.Water.SingleLayer.Reflection=1;------def 1------0 for PERFORMANCE
r.Water.SingleLayer.RefractionDownsampleFactor=4;------def 2------4 for PERFORMANCE------changed
r.Water.SingleLayer.RefractionFullPrecision=0;------def 0
r.Water.SingleLayer.RTR=1;------def 1
r.Water.SingleLayer.SSR=0;------def 1------0 for PERFORMANCE------changed
r.Water.SingleLayer.SSRTAA=0;------def 1------changed
r.Water.SingleLayer.TiledComposite=1;------def 1
RHI.SyncInterval=0;------def 1------changed
RHI.SyncSlackMS=0;------def 10------changed
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
InitialButtonRepeatDelay=0.2;------def 0.2
ButtonRepeatDelay=0.1;------def 0.1
DoubleClickTime=0.1;------def 0.25
```

---

<details><summary>Open GameUserSettings.ini these commands will overwrite your config so make sure they are correct also set your scalability groups 0 low 1 med  2 high 3 epic 4 cinematic, check for new stuff after updates</summary>
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
TextureStreamPoolSizeStorage=(Value=800)
MaxAnisotropy=(Value=)
FoliageMinLOD=(Value=1)
HZBOcclusion=(Value=)
ContactShadows=(Value=)
DetailMode=(Value=1)
AudioQualityLevel=3
MaxAnisotropy=8
bUseVSync=0
GlobalSensitivity=0.183
MaxFPS=
FrameRateLimit=
MenuFrameRateLimit=
HDRDisplayOutputNits=300;
DoubleKeyPressTime=0.1
DistanceFieldShadows=1;
Gamma=2.2
TAASampleStorage=4
bRTXEnabled=0
bRTXReflectionsEnabled=0
bRTXShadowsEnabled=0
bRTXAmbientOcclusionEnabled=0
DlssQualitySetting=1
ResolutionScaleModifier=1
DFAO=
Tessellation=0
TessellationMode=9999999
Tessellation=(Value=0)
TessellationMode=(Value=9999999)
bTelemetryEnabled=0
bUseDynamicResolution=0
FullscreenMode=0
PreferredFullscreenMode=0
ContactShadows=0
PostFX_Saturation=1.2
PostFX_Sharpness=0
OverrideOptions=(("r.PlaceHolder1", (Value=0,bModified=True)),("r.PlaceHolder2", (Value=1,bModified=False)));------works like engineini but in gameusersettingsini
OverrideOptions=(("r.Streaming.PoolSize", (Value=800,bModified=True)));------another example

[ScalabilityGroups]
sg.ResolutionQuality=100
sg.ViewDistanceQuality=2
sg.AntiAliasingQuality=2
sg.PostProcessQuality=2
sg.ShadowQuality=2
sg.TextureQuality=2
sg.EffectsQuality=2
sg.FoliageQuality=2
sg.ShadingQuality=2
sg.AnimationQuality=2
```

---

<details><summary>Open DeviceProfiles.ini and textures lods, WIP complicated to optimize</summary>
<p>
press <kbd>⊞ Win+R</kbd> then copy paste
<br>
%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
<br>
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
<br>
%localappdata%/ReadyOrNot/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
</p>
</details>

```python
WIP
```

---

#### in nvidia control panel

##### 1. 3D settings -> adjust image settings with preview -> use my preference emphasizing performance apply.

##### 2. click on use the advanced 3D image settings and apply then click "take me there"

##### 3. Anisotropic filtering:  set Application-controlled (you can force the setting in here if you can't notice it working in certain games)

##### 4. Antialiasing - mode: set Application-controlled 

##### 5. Low latency mode:

###### Off and ~85% gpu usage for multiple frame buffers sacrificing latency (cap fps til gpu usage is ~85%) (for visual fluidity of frames)

###### On forces 1 frame buffer (for lower latency than off) (for visual fluidity of frames)

###### Ultra and/or relfex (in-game) and ~97% gpu usage for lowest latency (could be less fluid frames at low fps)

##### 6. Power management mode:  prefer max performance  (this is the "+ boost" in reflex + boost)

##### 7. Preferred refresh rate:  Highest available

##### 8. Texture filtering - anisotropic sample optimization:  on  (off will look better if this even works in your game) (you may need to reapply because NVCP will reset when you change other settings)

##### 9. Texture filtering - negative LOD bias:  clamp  (this should be the default i.e. 0 mipmap bias) (you may need to reapply because NVCP will reset when you change other settings)

##### 10. Texture filtering quality:  high performance

##### 11. Texture filtering - trilinear optimization:  on

#####  12. Vertical sync:  Off

#####  13. Display -> Adjust desktop size and position -> set no scaling and Perform scaling on: Display

<details><summary>14. Turn on Message-signaled interrupts (MSIs) (better than line based interrupt method) click for how to</summary>
<p>
1. NVCleanstall enabling it in advanced settings before installing or
<br>
2. use Wtools enable it and restart or
<br>
3. find ID: open device manager right click your GPU properties and click on events tab
<br>
looks like this:
<br>
HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Enum\PCI\VEN_10DE&DEV_1E84&SUBSYS_139E10DE&REV_A1\4&3aaa5e18&0&0008\Device Parameters\Interrupt Management\MessageSignaledInterruptProperties
<br>
find in regedit and set MSISupported to 1 then restart
</p>
</details>
