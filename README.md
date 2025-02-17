## updated 2/16/2025 ✂ 📋 🌀 :ramen: v0.8.0

### for UE4 and UE5* games for reference/customization/optimization/learning

#### always testing stuff contact me [smoothschannel](https://twitch.tv/smoothschannel) or [discord](https://discord.gg/tDZT7QSx8m)

#### my config is trying to be quality and perform well for any UE4/5 game, it might not be perfectly optimal for a specific game

#### [Installing and optimizing nvidia drivers here](https://github.com/smo0ths/Installing-and-optimizing-new-nvidia-drivers-on-windows-11-gaming-PC)

#### check 🔴 options for more fps (left to right, performance to quality)

#### 2560x1440 use 🔴 58%,67%,70% for PERFORMANCE (higher when cpu bound) (DLSS/TAAU/TSR/CAS/FSR/XeSS/PSSR/NIS/IS)

#### 3328x1872 use 🔴 50%,58%,67% for PERFORMANCE (higher when cpu bound) (DLSS/TAAU/TSR/CAS/FSR/XeSS/PSSR/NIS/IS)

#### 3840x2160 use 🔴 33%,50%,58%,67% for PERFORMANCE (higher when cpu bound) (DLSS/TAAU/TSR/CAS/FSR/XeSS/PSSR/NIS/IS)

## Open Engine.ini and copy pasta %localappdata%

#### or Repak.bat method if it works (zzz_INIMODS\Engine\Config\Windows\WindowsEngine.ini)

```python
[Core.Log]
Global=off;
LogTelemetry=all off;

[CrashReportClient]
bAllowToBeContacted=0;
bIsAllowedToCloseWithoutSending=1;
bSendLogFile=0;
CanSendWhenUIFailedToInitialize=0;
DataRouterUrl="about:blank";
UIInitRetryCount=0;

[/Script/Engine.Engine]
bPauseOnLossOfFocus=0;
bSmoothFrameRate=0;
bUseFixedFrameRate=0;

[TextureStreaming]
PoolSizeVRAMPercentage=70; 🔴 50 to lower vram usage 🔵 texturepool cache

[ConsoleVariables]

; scaling stuff
r.AntiAliasingMethod=0; 🔵 0 off 1 FXAA 2 TAA 3 MSAA 4 TSR
r.CustomDepthTemporalAAJitter=1;
r.DynamicRes.OperationMode=0;
r.FidelityFX.FSR.Enabled=0; 🔵 FSR
r.FidelityFX.FSR.PrimaryUpscale=1;
r.FidelityFX.FSR.RCAS.Enabled=1;
r.FidelityFX.FSR.RCAS.Sharpness=0.2;
r.FidelityFX.FSR.SecondaryUpscale=1;
r.FidelityFX.FSR2.AutoExposure=0;
r.FidelityFX.FSR2.CreateReactiveMask=1;
r.FidelityFX.FSR2.Enabled=0; 🔵 FSR2
r.FidelityFX.FSR2.Sharpness=0;
r.FidelityFX.FSR2.UseSSRExperimentalDenoiser=0;
r.FidelityFX.FSR3.AutoExposure=0;
r.FidelityFX.FSR3.CreateReactiveMask=1;
r.FidelityFX.FSR3.Enabled=0; 🔵 FSR3
r.FidelityFX.FSR3.Sharpness=0;
r.FidelityFX.FSR3.UseSSRExperimentalDenoiser=0;
r.NGX.DLSS.AutoExposure=1;
r.NGX.DLSS.DilateMotionVectors=1;
r.NGX.DLSS.Enable=1; 🔵 DLSS
r.NGX.DLSS.PreferNISSharpen=0;
r.NGX.DLSS.Quality.Auto=0;
r.NGX.DLSS.Reflections.TemporalAA=0;
r.NGX.DLSS.Sharpness=0;
r.NGX.DLSS.WaterReflections.TemporalAA=0;
r.NIS.Enable=0; 🔵 NIS
r.NIS.Sharpness=0;
r.PostProcessAAQuality=0; 🔵 0 off 1,2 FXAA 3,4,5,6 TAA
r.SecondaryScreenPercentage.GameViewport=0;
r.SSR.ExperimentalDenoiser=0;
r.TemporalAA.Algorithm=0; 🔵 0,1 gen4,gen5 TAAU
r.TemporalAA.Upsampling=1; 🔴 0 for PERFORMANCE 🔵 TAAU
r.TemporalAASamples=8;
r.TSR.16BitVALU=0; 🟢 test
r.VRS.Enable=0;
r.VRS.EnableImage=0;
r.VRS.EnableSoftware=0;
r.XeSS.AutoExposure=1;
r.XeSS.Enabled=0; 🔵 XeSS
t.Streamline.Reflex.Enable=1; 🔵 reflex

; async stuff
fx.Niagara.AsyncGpuTrace.HWRayTraceEnabled=0;
r.Bloom.AsyncCompute=1;
r.d3d12.allowasynccompute=1;
r.DFShadowAsyncCompute=1; 🟢 test
r.Lumen.AsyncCompute=1;
r.Lumen.DiffuseIndirect.AsyncCompute=1;
r.Lumen.Reflections.AsyncCompute=1; 🟢 test
r.LumenScene.Lighting.AsyncCompute=1;
r.Nanite.AsyncRasterization.ShadowDepths=0;
r.Nanite.AsyncRasterization=1; 🟢 test
r.Nanite.Streaming.AsyncCompute=1;
r.SceneDepthHZBAsyncCompute=1; 🟢 test
r.SkyAtmosphereASyncCompute=1; 🟢 test
r.volumetricrendertarget.preferasynccompute=1; 🟢 test
r.vulkan.allowasynccompute=1;

; shaders
r.Shaders.RemoveDeadCode=1;
r.Shaders.RemoveUnusedInterpolators=1;

; nanite
r.GPUScene.ParallelUpdate=1; 🟢 test
r.Nanite.Streaming.Imposters=0;
r.Nanite.ViewMeshLODBias.Min=-2;
r.Nanite.ViewMeshLODBias.Offset=0;

; texture stuff
r.AnisotropicMaterials=1; 🔴 0 for PERFORMANCE
r.DetailMode=2; 🔴 0,1,2 for PERFORMANCE
r.LandscapeLODBias=0; 🔴 1 for PERFORMANCE
r.MaterialQualityLevel=1; 🔴 0,2 for PERFORMANCE
r.MaxAnisotropy=16; 🔴 0,4,8 for PERFORMANCE
r.OptimizedWPO=1;
r.Streaming.AmortizeCPUToGPUCopy=0;
r.Streaming.Boost=1;
r.Streaming.FullyLoadUsedTextures=0;
r.Streaming.HiddenPrimitiveScale=0.5; 🔴 0.5 for PERFORMANCE
r.Streaming.LimitPoolSizeToVRAM=1;
r.Streaming.MaxEffectiveScreenSize=0;
r.Streaming.MaxNumTexturesToStreamPerFrame=0;
r.Streaming.MipBias=0; 🔴 1 for PERFORMANCE
r.Streaming.PoolSize.VRAMPercentageClamp=1024;
r.Streaming.PoolSize=1000;
r.Streaming.PoolSizeForMeshes=-1;
r.Streaming.UseAllMips=0;
r.Streaming.UseFixedPoolSize=0;
r.Streaming.UsePerTextureBias=1;
r.SupportMaterialLayers=1; 🔴 0 for PERFORMANCE
r.TessellationAdaptivePixelsPerTriangle=999999; 🔴 999999,48 for PERFORMANCE
r.TextureStreaming=1;
r.VirtualTexture=0; 🟢 test
r.VirtualTexturedLightmaps=0; 🟢 test
r.VirtualTextureReducedMemory=0;
r.VirtualTextures=1;
r.VT.AnisotropicFiltering=1;
r.VT.MaxAnisotropy=8; 🔴 0,4 for PERFORMANCE
r.VT.MaxReleasedPerFrame=0; 🟢 test
r.VT.MaxTilesProducedPerFrame=96; 🟢 test
r.VT.MaxUploadsPerFrame.Streaming=48; 🟢 test
r.VT.MaxUploadsPerFrame=16; 🟢 test

; latency
D3D12.MaximumFrameLatency=1; 🔵 frame latency
r.D3D11.UseAllowTearing=1; 🔵 dxgi flip mode
r.D3D12.UseAllowTearing=1; 🔵 dxgi flip mode
r.GTSyncType=0;
r.VSync=0;
RHI.MaximumFrameLatency=1; 🔵 frame latency
t.MaxFPS=0;
t.OverrideFPS=0;

; occlusion system
r.HZBOcclusion=1;
r.NumBufferedOcclusionQueries=1; 🔵 frames to buffer occlusion queries test 1,2

; debug
r.D3D12.GPUCrashDebuggingMode=0;
r.DetectAndWarnOfBadDrivers=0;
r.ForceDebugViewModes=0;
r.gpucrash.collectionenable=0;
r.NGX.LogLevel=0;
r.VsyncInformationInsights=0;

; reflection
r.chaos.ReflectionCaptureStaticSceneOnly=1;
r.ReflectionCaptureResolution=128; 🔴 128 for PERFORMANCE
r.ReflectionCaptureSupersampleFactor=1;

; refraction
r.Refraction.Blur.TemporalAA=1; 🔵 temporal filtering
r.RefractionQuality=2; 🔴 0,1 for PERFORMANCE

; SSGI
r.SSGI.Enable=0; 🔴 0 for PERFORMANCE

; SSR
r.SSR.HalfResSceneColor=1; 🔴 1 for PERFORMANCE
r.SSR.Quality=2; 🔴 0,2 for PERFORMANCE

; sub surface scattering
r.SSS.Burley.Quality=0; 🔴 0 for PERFORMANCE
r.SSS.Checkerboard=1; 🔴 1 for PERFORMANCE
r.SSS.HalfRes=1; 🔴 1 for PERFORMANCE
r.SubsurfaceScattering=1; 🔴 0 for PERFORMANCE

; physics
p.AnimDynamics=1; 🔴 0 for PERFORMANCE
p.AnimDynamicsWind=1; 🔴 0 for PERFORMANCE
p.RigidBodyNode=1; 🔴 0 for PERFORMANCE

; particle
fx.Niagara.QualityLevel=3; 🔴 0,1,2 for PERFORMANCE
fx.NiagaraAllowRuntimeScalabilityChanges=1;
r.EmitterSpawnRateScale=1; 🔴 0.125,0.25,0.5 for PERFORMANCE
r.ParticleLightQuality=2; 🔴 0,1 for PERFORMANCE

; SSAO
r.AmbientOcclusionLevels=-1; 🔴 0,1 for PERFORMANCE
r.AmbientOcclusionMaxQuality=100;
r.AmbientOcclusionStaticFraction=-1; 🔴 0 for PERFORMANCE

; DFAO
r.AOQuality=2; 🔴 0 for PERFORMANCE

; post process stuff ect
r.Bloom.ScreenPercentage=50;
r.BloomQuality=4; 🔴 0 for PERFORMANCE
r.BlurGBuffer=0;
r.DepthOfFieldQuality=0; 🔴 0,1 for PERFORMANCE
r.DOF.Gather.AccumulatorQuality=0;
r.DOF.Gather.EnableBokehSettings=0;
r.DOF.Gather.PostfilterMethod=1;
r.DOF.Gather.RingCount=3;
r.DOF.Kernel.MaxBackgroundRadius=0.012;
r.DOF.Kernel.MaxForegroundRadius=0.012;
r.DOF.Recombine.Quality=0;
r.DOF.Scatter.BackgroundCompositing=0;
r.DOF.Scatter.EnableBokehSettings=0;
r.DOF.Scatter.ForegroundCompositing=0;
r.DOF.Scatter.MaxSpriteRatio=0.04;
r.DOF.TemporalAAQuality=0;
r.FilmGrain=0;
r.Filter.LoopMode=0; 🔴 0 for PERFORMANCE
r.Filter.SizeScale=1;
r.MotionBlurQuality=0;
r.PostProcessing.PreferCompute=1;
r.SceneColorFormat=3; 🔴 2,3 for PERFORMANCE
r.SceneColorFringe.Max=0;
r.SeparateTranslucencyAutoDownsample=1;
r.SeparateTranslucencyScreenPercentage=100;
r.Tonemapper.Quality=5;
r.Tonemapper.Sharpen=0;
r.Upscale.Quality=3; 🔴 1,2 for PERFORMANCE

; light
r.LightMaxDrawDistanceScale=1; 🔴 0.6 for PERFORMANCE
r.MinScreenRadiusForLights=0.03; 🔴 0.06,0.04 for PERFORMANCE

; hair
r.HairStrands.DeepShadow.SuperSampling=0;
r.HairStrands.Enable=1; 🔴 0 for PERFORMANCE
r.HairStrands.Interpolation.UseSingleGuide=1; 🔴 1 for PERFORMANCE
r.HairStrands.MinLOD=0;
r.HairStrands.RasterizationScale=0.5;
r.HairStrands.ScatterSceneLighting=1;
r.HairStrands.Shadow.CastShadowWhenNonVisible=0;
r.HairStrands.Simulation=1;
r.HairStrands.SkyAO.SampleCount=4;
r.HairStrands.SkyAO=0; 🔴 0 for PERFORMANCE
r.HairStrands.SkyLighting.IntegrationType=2;
r.HairStrands.SkyLighting.SampleCount=16;
r.HairStrands.SkyLighting=1;
r.HairStrands.UseCardsInsteadOfStrands=0; 🔴 1 for PERFORMANCE
r.HairStrands.VelocityRasterizationScale=1;
r.HairStrands.Visibility.MSAA.SamplePerPixel=4; 🔴 1,2 for PERFORMANCE
r.HairStrands.Visibility.PPLL=0; 🔴 0 for PERFORMANCE
r.HairStrands.Voxelization=0; 🔴 0 for PERFORMANCE

; HRT
r.DistanceFields.SupportEvenIfHardwareRayTracingSupported=0; 🟢 test
r.Lumen.HardwareRayTracing.LightingMode=0;
r.Lumen.HardwareRayTracing=0;
r.Lumen.RadianceCache.HardwareRayTracing.Retrace.FarField=0;
r.Lumen.RadianceCache.HardwareRayTracing=0;
r.Lumen.Reflections.HardwareRayTracing.Retrace.FarField=0;
r.Lumen.Reflections.HardwareRayTracing=0;
r.Lumen.ScreenProbeGather.HardwareRayTracing.Retrace.FarField=0;
r.Lumen.ScreenProbeGather.HardwareRayTracing=0;
r.Lumen.ScreenProbeGather.ShortRangeAO.HardwareRayTracing=0;
r.Lumen.TranslucencyVolume.HardwareRayTracing=0;
r.LumenScene.DirectLighting.HardwareRayTracing=0;
r.LumenScene.Radiosity.HardwareRayTracing=0;
r.ManyLights.HardwareRayTracing=0;

; lumen
r.GBufferDiffuseSampleOcclusion=1; 🔵 bent normal maps
r.Lumen.DiffuseIndirect.Allow=1; 🔴 0 for PERFORMANCE 🔵 lumen global illumination
r.Lumen.DiffuseIndirect.SSAO=0;
r.Lumen.IrradianceFieldGather=0; 🔵 experimental
r.Lumen.RadianceCache.NumFramesToKeepCachedProbes=8;
r.Lumen.Reflections.Allow=1; 🔴 0 for PERFORMANCE 🔵 lumen reflections
r.Lumen.Reflections.BilateralFilter.NumSamples=4;
r.Lumen.Reflections.BilateralFilter.SpatialKernelRadius=0.002;
r.Lumen.Reflections.BilateralFilter=1;
r.Lumen.Reflections.DownsampleFactor=1; 🔴 2 for PERFORMANCE
r.Lumen.Reflections.MaxRoughnessToTrace=0.4;
r.Lumen.Reflections.MaxRoughnessToTraceForFoliage=0.4;
r.Lumen.Reflections.RadianceCache=1; 🔵 radiance cache
r.Lumen.Reflections.ScreenSpaceReconstruction.TonemapStrength=0;
r.Lumen.Reflections.ScreenSpaceReconstruction=1; 🔵 reconstruction
r.Lumen.Reflections.Temporal=1; 🔵 temporal filtering
r.Lumen.Reflections.TraceMeshSDFs=0; 🔴 0 for PERFORMANCE
r.Lumen.SampleFog=0;
r.Lumen.ScreenProbeGather.DownsampleFactor=16; 🔴 32 for PERFORMANCE
r.Lumen.ScreenProbeGather.IrradianceFormat=1; 🔴 1 for PERFORMANCE
r.Lumen.ScreenProbeGather.MaterialAO=1;
r.Lumen.ScreenProbeGather.RadianceCache=1; 🔵 persistent world space radiance cache
r.Lumen.ScreenProbeGather.ScreenSpaceBentNormal=1; 🔵 bent normal maps, changed to ShortRangeAO
r.Lumen.ScreenProbeGather.ShortRangeAO.ApplyDuringIntegration=0;
r.Lumen.ScreenProbeGather.ShortRangeAO=1;
r.Lumen.ScreenProbeGather.StochasticInterpolation=1; 🔴 1 for PERFORMANCE
r.Lumen.ScreenProbeGather.Temporal=1; 🔵 temporal filtering
r.Lumen.ScreenProbeGather.TraceMeshSDFs=0; 🔴 0 for PERFORMANCE 🔵 software lumen
r.Lumen.ScreenProbeGather.TracingOctahedronResolution=8;
r.Lumen.ScreenProbeGather.TwoSidedFoliageBackfaceDiffuse=1;
r.Lumen.TraceMeshSDFs.Allow=0; 🔴 0 for PERFORMANCE 🔵 software lumen
r.Lumen.TraceMeshSDFs.TraceDistance=180; 🔴 90 for PERFORMANCE
r.Lumen.TraceMeshSDFs=0; 🔴 0 for PERFORMANCE
r.Lumen.TranslucencyReflections.FrontLayer.Allow=1; 🔴 0 for PERFORMANCE
r.Lumen.TranslucencyReflections.FrontLayer.Enable=1; 🔴 0 for PERFORMANCE
r.Lumen.TranslucencyVolume.Enable=1;
r.LumenScene.DirectLighting.OffscreenShadowing.TraceMeshSDFs=0;
r.LumenScene.FarField=0;

; shadow
r.AllowLandscapeShadows=1; 🔴 0 for PERFORMANCE
r.CapsuleShadows=1; 🔴 0 for PERFORMANCE
r.ContactShadows=1; 🔴 0 for PERFORMANCE
r.DFFullResolution=0; 🔴 0 for PERFORMANCE
r.DFShadowQuality=2; 🔴 1,2 for PERFORMANCE
r.HeightFieldShadowing=0; 🔵 height field shadowing
r.Shadow.CSM.MaxCascades=2; 🔴 1,2,4 for PERFORMANCE
r.Shadow.CSMShadowDistanceFadeoutMultiplier=1;
r.Shadow.DistanceScale=1; 🔴 0.7 for PERFORMANCE
r.Shadow.ForceSingleSampleShadowingFromStationary=0; 🔴 1 for PERFORMANCE
r.Shadow.MaxCSMResolution=2048; 🔴 512,1024 for PERFORMANCE
r.Shadow.MaxResolution=2048; 🔴 512,1024 for PERFORMANCE
r.Shadow.NaniteLODBias=1; 🔴 1 for PERFORMANCE
r.Shadow.RadiusThreshold=0.03; 🔴 0.06,0.05,0.04 for PERFORMANCE
r.Shadow.Virtual.Cache.StaticSeparate=1;
r.Shadow.Virtual.DistantLightMode=1;
r.Shadow.Virtual.NonNanite.IncludeInCoarsePages=0; 🔴 0 for PERFORMANCE
r.Shadow.Virtual.NonNanite.ParallelSinglePassBatched=1;
r.Shadow.Virtual.NonNanite.SinglePassBatched=1;
r.Shadow.Virtual.OnePassProjection.MaxLightsPerPixel=8; 🔴 8 for PERFORMANCE
r.Shadow.Virtual.OnePassProjection=1; 🔴 1 for PERFORMANCE 🔵 experimental one pass projection
r.Shadow.Virtual.PageMarkingPixelStrideX=2;
r.Shadow.Virtual.PageMarkingPixelStrideY=2;
r.Shadow.Virtual.SMRT.AdaptiveRayCount=1; 🟢 test
r.Shadow.Virtual.SMRT.ExtrapolateMaxSlopeLocal=0.05;
r.Shadow.Virtual.SMRT.MaxRayAngleFromLight=0.03;
r.Shadow.Virtual.SMRT.MaxSlopeBiasLocal=50;
r.Shadow.Virtual.SMRT.RayCountDirectional=4; 🔴 2,4 for PERFORMANCE
r.Shadow.Virtual.SMRT.RayCountLocal=4; 🔴 2,4 for PERFORMANCE
r.Shadow.Virtual.SMRT.RayLengthScaleDirectional=1.5;
r.Shadow.Virtual.SMRT.ReduceRaysAtDistance=1;
r.Shadow.Virtual.SMRT.SamplesPerRayDirectional=2; 🔴 1,2 for PERFORMANCE
r.Shadow.Virtual.SMRT.SamplesPerRayLocal=2; 🔴 1,2 for PERFORMANCE
r.Shadow.Virtual.SMRT.TexelDitherScaleDirectional=2;
r.Shadow.Virtual.SMRT.TexelDitherScaleLocal=2;
r.Shadow.Virtual.SubsurfaceShadowMode=1;
r.Shadow.Virtual.TranslucentQuality=0; 🔴 0 for PERFORMANCE
r.ShadowQuality=4; 🔴 3,4 for PERFORMANCE
r.TranslucencyLightingVolumeDim=48; 🔴 32,48 for PERFORMANCE
r.TranslucencyVolumeBlur=1; 🔴 0 for PERFORMANCE
r.UseClusteredDeferredShading=0; 🔵 clustered deferred shading

; sky
r.SkyAtmosphere.FastSkyLUT.SampleCountMax=64; 🔴 32,64 for PERFORMANCE
r.SkyAtmosphere.FastSkyLUT.SampleCountMin=1; 🔴 1 for PERFORMANCE
r.SkyAtmosphere.LUT32=0; 🔴 0 for PERFORMANCE
r.SkyAtmosphere.MultiScatteringLUT.HighQuality=0; 🔴 0 for PERFORMANCE
r.SkyAtmosphere.MultiScatteringLUT.SampleCount=15;
r.SkyAtmosphere.SampleCountMax=64; 🔴 32,64 for PERFORMANCE
r.SkyAtmosphere.SampleCountMin=1; 🔴 1 for PERFORMANCE
r.SkyAtmosphere.SampleLightShadowmap=0; 🔴 0 for PERFORMANCE 🔵 volumetric shadows
r.SkyAtmosphere.TransmittanceLUT.SampleCount=10;
r.SkyAtmosphere.TransmittanceLUT.UseSmallFormat=0; 🔴 1 for PERFORMANCE

; clouds
r.VolumetricCloud.DistanceToSampleMaxCount=15;
r.VolumetricCloud.EnableAtmosphericLightsSampling=1;
r.VolumetricCloud.EnableDistantSkyLightSampling=1;
r.VolumetricCloud.EnableLocalLightsSampling=0; 🔴 0 for PERFORMANCE 🔵 experimental
r.VolumetricCloud.Shadow.SampleAtmosphericLightShadowmap=0; 🔴 0 for PERFORMANCE 🔵 volumetric shadows
r.VolumetricCloud.ShadowMap.SpatialFiltering=1; 🔵 cloud shadow blur
r.VolumetricCloud.ShadowMap=1;
r.VolumetricCloud.SkyAO=1;
r.VolumetricCloud=1; 🔴 0 for PERFORMANCE

; fog
r.Fog=1; 🔵 render fog
r.VolumetricFog.ConservativeDepth=0; 🔵 experimental
r.VolumetricFog.DepthDistributionScale=32; 🔴 16 for PERFORMANCE
r.VolumetricFog.Emissive=0; 🟢 test
r.VolumetricFog.GridPixelSize=16; 🔴 16 for PERFORMANCE
r.VolumetricFog.GridSizeZ=96; 🔴 64 for PERFORMANCE
r.VolumetricFog.HistoryMissSupersampleCount=2; 🔴 2 for PERFORMANCE
r.VolumetricFog.Jitter=1; 🔵 temporal filtering
r.VolumetricFog.TemporalReprojection=1;
r.VolumetricFog.UpsampleJitterMultiplier=1; 🔴 0 for PERFORMANCE
r.VolumetricFog=1; 🔴 0 for PERFORMANCE

; water
r.Water.EnableShallowWaterSimulation=0; 🔴 0 for PERFORMANCE
r.Water.EnableUnderwaterPostProcess=0; 🔴 0 for PERFORMANCE
r.Water.Reflections.MaxRoughnessToTrace=1;
r.Water.SingleLayer.DepthPrepass=1;
r.Water.SingleLayer.DistanceFieldShadow=1;
r.Water.SingleLayer.DownsampleReflections=1; 🔴 1 for PERFORMANCE
r.Water.SingleLayer.Reflection=1; 🔵 reflection technique
r.Water.SingleLayer.RefractionDownsampleFactor=1; 🔴 1,2 for PERFORMANCE
r.Water.SingleLayer.RTR=0; 🔴 0 for PERFORMANCE
r.Water.SingleLayer.ShadersSupportDistanceFieldShadow=1;
r.Water.SingleLayer.ShadersSupportVSMFiltering=1;
r.Water.SingleLayer.SSR=0; 🔴 0 for PERFORMANCE
r.Water.SingleLayer.TiledComposite=1;
r.Water.SingleLayer.UnderwaterFogWhenCameraIsAboveWater=0;
r.Water.SingleLayer.VSMFiltering=1;
r.Water.WaterMesh.TessFactorBias=0; 🔴 -1 for PERFORMANCE
```

---

## Open Input.ini and copy pasta %localappdata%

#### or Repak.bat method if it works (zzz_INIMODS\Engine\Config\Windows\WindowsInput.ini)

```python
[/Script/Engine.InputSettings]
bAltEnterTogglesFullscreen=1;
bEnableMouseSmoothing=0;
bF11TogglesFullscreen=0;
ButtonRepeatDelay=0.1;
bViewAccelerationEnabled=0;
DoubleClickTime=0.01; 🔵 def 0.1
InitialButtonRepeatDelay=0.1; 🔵 def 0.2
```

---

## Open GameUserSettings.ini these commands can overwrite your config if they are here %localappdata%

#### you can turn down used scalability groups here or in game if they are being used

```python
[ScalabilityGroups]
sg.AntiAliasingQuality=?;
sg.EffectsQuality=?;
sg.FoliageQuality=?;
sg.GlobalIlluminationQuality=?;
sg.LandscapeQuality=?;
sg.PostProcessQuality=?;
sg.ReflectionQuality=?;
sg.ShadingQuality=?;
sg.ShadowQuality=?;
sg.TextureQuality=?;
sg.ViewDistanceQuality=?;

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
MaterialQuality=(Value=?);
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
```

---

## Open DeviceProfiles.ini for textures lods, mess around but its best to leave these alone unless you are dev %localappdata%

```python
there is more like TEXTUREGROUP_Project01,TEXTUREGROUP_Project02 and custom asset names like TEXTUREGROUP_goodtrees
MaxLODSize_VT=0,OptionalLODBias=0,MipLoadOptions=AllMips,HighPriorityLoad=False,DuplicateNonOptionalMips=False,
Downscale=1,DownscaleOptions=SimpleAverage,VirtualTextureTileCountBias=0,VirtualTextureTileSizeBias=0,LossyCompressionAmount=TLCA_Default
```

```python
[/Script/Engine.TextureLODSettings]
TextureLODGroups=(Group=TEXTUREGROUP_World,                 MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WorldNormalMap,        MinLODSize=256,  MaxLODSize=2048, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WorldSpecular,         MinLODSize=256,  MaxLODSize=2048, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Character,             MinLODSize=512,  MaxLODSize=4096, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_CharacterNormalMap,    MinLODSize=256,  MaxLODSize=2048, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_CharacterSpecular,     MinLODSize=256,  MaxLODSize=2048, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_Weapon,                MinLODSize=256,  MaxLODSize=2048, OptionalMaxLODSize=1024, LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WeaponNormalMap,       MinLODSize=128,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
TextureLODGroups=(Group=TEXTUREGROUP_WeaponSpecular,        MinLODSize=128,  MaxLODSize=1024, OptionalMaxLODSize=512,  LODBias=0, MinMagFilter=aniso,  MipFilter=point,  MipGenSettings=TMGS_SimpleAverage, NumStreamedMips=-1);
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
