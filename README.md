~~~~~~~~~~~~~~~~~~~~~~~~~


*Updated 12/28/2021~~~~~

*For UE4 games for reference/customization/optimization/learning

*Discord link discord.gg/vB8f4fZ7EH

*Always testing stuff contact me twitch.tv/smoothschannel or discord


-----------end-----------


Open Engine.ini

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Engine.ini 
Copy/Paste:  %localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Engine.ini
Copy/Paste:  %localappdata%/BendGame/Saved/Config/WindowsNoEditor/Engine.ini


my config is more of a quality balance you may need to tweak some commands, copy and paste under code

[Core.Log]
Global=off;

[Audio]
MaxChannels=64;--------------------------32 48 64 96 128 LOWER VALUES for PERFORMANCE
CommonAudioPoolSize=0;--------------------------default 0
UnfocusedVolumeMultiplier=1;

[/Script/Engine.Engine]
bSmoothFrameRate=0;
bPauseOnLossOfFocus=0;
bUseFixedFrameRate=0;
DisplayGamma=2.2;

[TextureStreaming]
PoolSizeVRAMPercentage=70;--------------------------TEXTUREPOOL CACHE LOWER IF YOU RUN OUT OF VRAM

[ConsoleVariables]
FX.BatchAsync=1;
FX.AllowAsyncTick=1;
FX.EarlyScheduleAsync=0;--------------------------TEST
FX.BatchAsyncBatchSize=32;
FX.AllowCulling=1;
r.ShaderDevelopmentMode=0;
r.Atmosphere=1;
r.VSync=0;
r.AllowHDR=0;
r.HDR.EnableHDROutput=0;
r.GPUCrashDebugging=0;
r.AsyncPipelineCompile=1;
r.CompileShadersForDevelopment=0;--------------------------default 1
r.CreateShadersOnLoad=0;--------------------------TEST
r.EarlyZPass=2;--------------------------default 3
r.EarlyZPassMovable=1;
r.EarlyZPassOnlyMaterialMasking=1;
r.DBuffer=1;--------------------------DECAL METERIAL BLEND MODES 0 for PERFORMANCE default 1
r.FinishCurrentFrame=0;
r.GTSyncType=0;
rhi.SyncSlackMS=0;
r.UniformBufferPooling=1;
r.DrawRectangleOptimization=1;--------------------------default 1
r.AlsoUseSphereForFrustumCull=0;--------------------------TEST 0 for PERFORMANCE
r.DoInitViewsLightingAfterPrepass=0;--------------------------TEST 1 IS EXPERIMENTAL
r.DoLazyStaticMeshUpdate=0;--------------------------1 IS EXPERIMENTAL MESHES FLICKER ON 1
r.DeferUniformBufferUpdatesUntilVisible=1;--------------------------TEST
r.DeferUniformExpressionCaching=1;--------------------------TEST
r.DeferSkeletalDynamicDataUpdateUntilGDME=0;--------------------------TEST 1 IS EXPERIMENTAL
r.MeshStreaming=0;--------------------------1 IS EXPERIMENTAL
r.DiscardUnusedQuality=0;--------------------------1 CRASHES GAMES default 0
r.RenderTargetPoolMin=400;
r.MorphTarget.Mode=1;--------------------------0 CPU METHOD 1 GPU METHOD default 1
r.VertexFoggingForOpaque=1;
r.GenerateMeshDistanceFields=1;--------------------------0 for PERFORMANCE
r.NormalMapsForStaticLighting=0;
r.GenerateLandscapeGIData=0;--------------------------0 for PERFORMANCE
r.AllowGlobalClipPlane=0;
r.LightingDetailMode=150;--------------------------50 OR 100 for PERFORMANCE default 150
r.HZBOcclusion=0;--------------------------OCCLUSION CULLING ALGORITHM default 1
r.AllowOcclusionQueries=1;
r.OneFrameThreadLag=1;--------------------------1 GAME SYNC WITH RENDER THREAD
r.AllowSubPrimitiveQueries=1;
r.SceneColorFormat=4;--------------------------3 for PERFORMANCE default 4
r.DefaultBackBufferPixelFormat=4;--------------------------default 4
r.ClearSceneMethod=1;
r.ClearWithExcludeRects=2;--------------------------default 2
r.GBufferFormat=1;--------------------------default 1
r.LightFunctionQuality=1;--------------------------0 or 1 for PERFORMANCE default 2
r.ClearCoatNormal=0;--------------------------0 for PERFORMANCE
Compat.UseDXT5NormalMaps=0;
r.MinScreenRadiusForLights=0.015;--------------------------TEST default 0.03
r.MinScreenRadiusForDepthPrepass=0.03;--------------------------default 0.03
r.MinScreenRadiusForCSMDepth=0.01;
r.SkyLightingQuality=1;--------------------------TEST 0 for PERFORMANCE
r.SupportStationarySkylight=1;
r.SkylightIntensityMultiplier=0.8;--------------------------SKYLIGHT INTENSITY
r.LightMaxDrawDistanceScale=1;--------------------------DYNAMIC LIGHTS LOD SCALE 0 OR 0.5 for PERFORMANCE
r.MipMapLODBias=0;--------------------------LODS
r.LandscapeLODBias=0;
r.SkeletalMeshLODBias=0;
r.ParticleLODBias=-1;
r.LandscapeLODDistributionScale=1;
r.LandscapeLOD0DistributionScale=1;
r.ViewDistanceScale=1;--------------------------VIEW DISTANCE 0.8 for PERFORMANCE
r.ViewDistanceScale.FieldOfViewAffectsHLOD=0;
r.SkeletalMeshLODRadiusScale=1;--------------------------LOWER for QUALITY 0.25-1 default 1
r.StaticMeshLODDistanceScale=1;--------------------------LOWER for QUALITY 0.25-1 default 1
r.SplineMesh.NoRecreateProxy=1;
r.TextureStreaming=1;--------------------------TEXTURE STREAMING
r.Streaming.MipBias=0;
r.Streaming.UseFixedPoolSize=0;
r.Streaming.LimitPoolSizeToVRAM=1;
r.Streaming.PoolSize=1024;
r.Streaming.MaxTempMemoryAllowed=50;--------------------------TEST
r.Streaming.PoolSize.VRAMPercentageClamp=1024;
r.Streaming.UseAllMips=0;
r.Streaming.MaxEffectiveScreenSize=0;
r.Streaming.Boost=1;
r.Streaming.UsePerTextureBias=1;
r.Streaming.AmortizeCPUToGPUCopy=1;
r.Streaming.MaxNumTexturesToStreamPerFrame=1;
r.Streaming.FramesForFullUpdate=10;
r.Streaming.NumStaticComponentsProcessedPerFrame=50;
r.Streaming.FullyLoadUsedTextures=0;
r.Streaming.DefragDynamicBounds=1;
r.Streaming.ScaleTexturesByGlobalMyBias=1;
r.Streaming.HiddenPrimitiveScale=0.5;--------------------------default 0.5
r.Streaming.UseNewMetrics=1;
r.Streaming.MinMipForSplitRequest=1;
r.Streaming.UseMaterialData=1;
r.Streaming.MaxHiddenPrimitiveViewBoost=0.5;
r.Streaming.PerTextureBiasViewBoostThreshold=0.5;
r.Streaming.MinLevelTextureScreenSize=100;
r.Streaming.MipCalculationEnablePerLevelList=1;
r.Streaming.OverlapAssetAndLevelTicks=0;
r.Streaming.UseBackgroundThreadPool=1;
r.DistanceFieldGI=0;
r.DistanceFieldAO=0;--------------------------DFAO 0 for PERFORMANCE
r.AOQuality=2;--------------------------0 for PERFORMANCE default 2
r.ShadowQuality=3;--------------------------SHADOWS
r.Shadow.FilterMethod=0;
r.Shadow.MaxResolution=1024;
r.Shadow.MaxCSMResolution=2048;
r.Shadow.CSM.MaxCascades=2;--------------------------TEST 1 or 2 for PERFORMANCE
r.Shadow.CSM.TransitionScale=1;
r.Shadow.RadiusThreshold=0.01;--------------------------default 0.03
r.Shadow.DistanceScale=1;--------------------------0.6 for PERFORMANCE
r.Shadow.CachedShadowsCastFromMovablePrimitives=1;--------------------------0 for PERFORMANCE
r.Shadow.MaxCSMStaticCachedShadowResolution=1024;--------------------------TEST
r.ContactShadows=0;--------------------------0 for PERFORMANCE
r.ContactShadows.NonShadowCastingIntensity=0.2;
r.CapsuleShadows=0;--------------------------0 for PERFORMANCE
r.AllowLandscapeShadows=1;--------------------------LANDSCAPE SHADOWS 0 for PERFORMANCE
r.DistanceFieldShadowing=1;--------------------------DISTANCE FIELD SHADOWING 0 for PERFORMANCE
r.DFShadowQuality=3;--------------------------1 to 3 QUALITY VALUES 0 OFF default 3
r.Shadow.MaxNumFarShadowCascades=1;--------------------------0 for PERFORMANCE
r.DFFullResolution=0;--------------------------0 for PERFORMANCE
r.DFShadowScatterTileCulling=1;--------------------------1 IS OPTIMAL
r.DFTwoSidedMeshDistanceBias=0;--------------------------0 for PERFORMANCE
r.DFDistanceScale=1;--------------------------default 1
r.Tonemapper.Quality=2;
r.TonemapperFilm=1;
r.Tonemapper.GrainQuantization=1;--------------------------FIGHTS 8 BIT COLOR BANDING default 1
r.Tonemapper.Sharpen=0;
r.Tonemapper.MergeWithUpscale.Mode=0;
ShowFlag.Vignette=0;
ShowFlag.Grain=0;
r.MinRoughnessOverride=0.2;--------------------------0.2 WITHOUT TAA 0 WITH TAA
r.DefaultFeature.AntiAliasing=0;--------------------------0 OFF 1 FXAA 2 TAA 3 MSAA
r.PostProcessAAQuality=0;--------------------------0 OFF 1 TO 2 FXAA 3 TO 6 TAA
r.MSAACount=0;
r.TemporalAASamples=4;
r.TemporalAAFilterSize=1;
r.TemporalAACurrentFrameWeight=0;
r.TemporalAA.R11G11B10History=0;--------------------------1 IS EXPERIMENTAL
r.TemporalAA.Algorithm=0;--------------------------1 IS EXPERIMENTAL
r.TemporalAA.Upsampling=0;--------------------------TAAU
r.TemporalAAUpsampleFiltered=0;
r.ScreenPercentage=100;--------------------------INPUT RESOLUTION PERCENTAGE for TAAU
r.SceneRenderTargetResizeMethodForceOverride=1;
r.SceneRenderTargetResizeMethod=0;--------------------------default 0
r.SceneCaptureResizeMethod=0;--------------------------default 0
r.Upscale.Quality=3;--------------------------default 3
r.EnableAsyncComputeTranslucencyLightingVolumeClear=1;--------------------------TEST
r.TranslucencyLightingVolume=1;--------------------------TRANSLUCENCY LIGHT VOLUME
r.TranslucencyVolumeBlur=1;
r.TranslucencyLightingVolumeDim=48;
p.BatchPhysXTasksSize=3;--------------------------TEST
p.ClothPhysics=1;--------------------------default 1
p.AnimDynamics=1;
p.AnimDynamicsWind=1;--------------------------0 for PERFORMANCE
p.AnimDynamicsLODThreshold=0;--------------------------0 for PERFORMANCE
p.RigidBodyLODThreshold=0;--------------------------0 for PERFORMANCE
p.AnimDynamicsAdaptiveSubstep=1;--------------------------TEST
p.AnimDynamicsRestrictLOD=-1;--------------------------TEST
r.SeparateTranslucency=0;--------------------------TEST
r.TranslucentSortPolicy=0;
r.AmbientOcclusionLevels=2;--------------------------SSAO 0 for PERFORMANCE
r.DefaultFeature.AmbientOcclusionStaticFraction=0;--------------------------0 for PERFORMANCE
r.AmbientOcclusionStaticFraction=0;--------------------------0 for PERFORMANCE
r.AmbientOcclusionMipLevelFactor=0.5;--------------------------default 0.5
r.AmbientOcclusionMaxQuality=100;
r.AmbientOcclusionSampleSetQuality=-1;
r.AmbientOcclusion.Compute=0;
r.AmbientOcclusionRadiusScale=0;
r.LightShaftQuality=1;--------------------------LIGHT SHAFTS 0 for PERFORMANCE
r.LightShaftDownSampleFactor=2;
r.LightShaftFirstPassDistance=0.1;
r.LightShaftBlurPasses=3;
r.LightShaftNumSamples=12;
r.LightShaftRenderToSeparateTranslucency=0;
r.SupportSkyAtmosphere=1;
r.SupportSkyAtmosphereAffectsHeightFog=1;
r.SupportAtmosphericFog=1;
r.Fog=1;
r.VolumetricFog=1;--------------------------0 for PERFORMANCE
r.VolumetricFog.GridPixelSize=32;
r.VolumetricFog.GridSizeZ=64;
r.VolumetricFog.HistoryWeight=0.9;
r.VolumetricFog.InjectShadowedLightsSeparately=0;
r.VolumetricFog.TemporalReprojection=1;
r.VolumetricFog.HistoryMissSupersampleCount=1;
r.ReflectionEnvironment=1;--------------------------REFLECTION ENVIRONMENT 0 for PERFORMANCE
r.chaos.ReflectionCaptureStaticSceneOnly=1;--------------------------1 for PERFORMANCE default 1
r.ReflectionCaptureGPUArrayCopy=1;
r.ReflectionCaptureResolution=128;--------------------------default 128
r.ReflectionEnvironmentCubemapPoolFixedNum=128;--------------------------TEST
r.ReflectionEnvironmentLightmapMixing=1;
r.DoTiledReflections=1;--------------------------TILED REFLECTION default 1
r.TiledDeferredShading=1;--------------------------TILED DEFERRED SHADING 0 for PERFORMANCE
r.TiledDeferredShading.MinimumCount=80;--------------------------LOWER for PERFORMANCE default 80
r.SSR.Quality=0;--------------------------SSR 0 for PERFORMANCE
r.SSR.HalfResSceneColor=0;--------------------------1 for PERFORMANCE
r.SSR.MaxRoughness=0.8;
r.SSGI.Enable=0;
r.SSGI.Quality=0;--------------------------SSGI 1 TO 4 QUALITY VALUES 0 OFF
r.SSGI.HalfRes=0;--------------------------1 for PERFORMANCE
r.SSGI.LeakFreeReprojection=0;--------------------------default 0
r.SubsurfaceScattering=1;--------------------------SSS 0 for PERFORMANCE
r.SSS.Scale=1;--------------------------default 1
r.SSS.SampleSet=2;--------------------------0 for PERFORMANCE default 2
r.SSS.Quality=-1;--------------------------default 0
r.SSS.HalfRes=0;--------------------------1 for PERFORMANCE
r.SSS.Filter=1;
r.SSS.Checkerboard=1;
r.ParticleLightQuality=2;--------------------------PARTICLES 0 or 1 for PERFORMANCE
r.ParticleMinTimeBetweenTicks=10;
r.EmitterSpawnRateScale=1;--------------------------0.25 or 0.5 for PERFORMANCE
r.MaxAnisotropy=8;
r.SupportMaterialLayers=1;
r.TessellationAdaptivePixelsPerTriangle=48;--------------------------9999999 for PERFORMANCE default 48
r.MaterialQualityLevel=1;--------------------------0 for PERFORMANCE
r.DetailMode=1;--------------------------0 for PERFORMANCE
r.RefractionQuality=1;--------------------------0 or 1 for PERFORMANCE default 2
r.IrisNormal=1;--------------------------0 for PERFORMANCE
r.DepthOfFieldQuality=0;--------------------------DOF 0 for PERFORMANCE
r.Filter.SizeScale=1;--------------------------default 1
r.Filter.NewMethod=1;
r.Filter.LoopMode=0;
r.BloomQuality=3;--------------------------BLOOM
r.Bloom.HalfResolutionFFT=0;
r.Bloom.Cross=0;--------------------------use -0.7777 for ANAMORPHIC BLOOM default 0
r.MotionBlurQuality=0;
r.FastBlurThreshold=0;
r.LensFlareQuality=2;--------------------------LENS FLARES 0 for PERFORMANCE default 2
r.SceneColorFringeQuality=0;
r.SceneColorFringe.Max=-1;
grass.DensityScale=0.6;--------------------------0.6 for PERFORMANCE
grass.DisableDynamicShadows=0;--------------------------1 for PERFORMANCE
foliage.DensityScale=0.6;--------------------------0.6 for PERFORMANCE
foliage.MinVertsToSplitNode=8192;--------------------------default 8192
foliage.DitheredLOD=1;--------------------------1 DITHERED 0 POPPING LOD
r.Decal.FadeDurationScale=1;--------------------------0.6 for PERFORMANCE default 1
r.Decal.FadeScreenSizeMult=1;
r.Decal.StencilSizeThreshold=0.1;--------------------------default 0.1
r.Decal.GenerateRTWriteMaskTexture=0;



-----------end-----------

Open Input.ini

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Input.ini
Copy/Paste:  %localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Input.ini


edit input commands or add them

[/Script/Engine.InputSettings] 
bAltEnterTogglesFullscreen=1;
bF11TogglesFullscreen=0; 
bEnableMouseSmoothing=0;
bViewAccelerationEnabled=0;
InitialButtonRepeatDelay=0.1;--------------------------TEST default 0.2
ButtonRepeatDelay=0.1;


-----------end-----------


Open GameUserSettings.ini

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/GameUserSettings.ini
Copy/Paste:  %localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/GameUserSettings.ini


here are a few things to look for or tweak these overwrite engine.ini commands unfortunately

bRTXEnabled=True
bRTXReflectionsEnabled=False
bRTXShadowsEnabled=False
bRTXAmbientOcclusionEnabled=False
DlssQualitySetting=1
bTelemetryEnabled=0
bUseVSync=0 
FullscreenMode=0
LastConfirmedFullscreenMode=0
PreferredFullscreenMode=0
HDRDisplayOutputNits=
bUseDynamicResolution=0
AudioQualityLevel=3
LastConfirmedAudioQualityLevel=3
FrameRateLimit=            
MenuFrameRateLimit=
MaxAnisotropy=
ContactShadows=0
PostFX_Saturation=1.200000
PostFX_Sharpness=0.000000
DistanceFieldShadows=1
TextureStreamPoolSizeStorage=1024
OverrideOptions=(("r.somerandomcommand", (Value=0,bModified=True)),("r.someotherrandomcommand", (Value=0,bModified=False))) ; if you want to override from GameUserSettings.ini


set your scalability groups

[ScalabilityGroups]
sg.ResolutionQuality=100.000000
sg.ViewDistanceQuality=0
sg.AntiAliasingQuality=0
sg.ShadowQuality=0
sg.PostProcessQuality=0
sg.TextureQuality=0
sg.EffectsQuality=0
sg.FoliageQuality=0
sg.ShadingQuality=0


-----------end-----------


Open DeviceProfiles.ini

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
Copy/Paste:  %localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/DeviceProfiles.ini


textures or you can just use in game settings (sg.TextureQuality=) copy and paste

[/Script/Engine.TextureLODSettings]
TextureLODGroups=(Group=TEXTUREGROUP_World,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverag,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_WorldNormalMap,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_WorldSpecular,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Character,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_CharacterNormalMap,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_CharacterSpecular,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Weapon,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_WeaponNormalMap,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_WeaponSpecular,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Vehicle,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_VehicleNormalMap,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_VehicleSpecular,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Effects,MinLODSize=1,MaxLODSize=1024,LODBias=0,MinMagFilter=linear,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_EffectsNotFiltered,MinLODSize=1,MaxLODSize=1024,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Skybox,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_UI,MinLODSize=1,MaxLODSize=1024,LODBias=0,MinMagFilter=linear,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Lightmap,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_Shadowmap,MinLODSize=256,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)
TextureLODGroups=(Group=TEXTUREGROUP_RenderTarget,MinLODSize=1,MaxLODSize=1024,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=-1)


-----------end-----------


for NVIDIA users:

Turn on Message-signaled interrupts (MSIs)

Adjust image settings set to Performance and apply then Select Use the advanced 3D image settings and apply

In manage 3D settings:

Anisotropic filtering:  Off for perf. App-controlled or force your own setting for quality

Low latency mode:  
1. Off and ~85% gpu usage for most med-lower end systems (assuming you cap fps correctly)
2. On feels consistent (i use this and reflex in games that support it)
3. Ultra and relfex (in-game) feels good when gpu usage is ~97%

Power management mode:  Prefer max performance  (this is the "+ boost" in reflex + boost)

Preferred refresh rate:  Highest available

Texture filtering - anisotropic sample optimization:  on

Texture filtering - Negative LOD bias:  Allow

Texture filtering quality:  High performance

Vertical sync:  Off


-----------end-----------


How to enable Message-signaled interrupts (MSIs):

use Wtools v1.0.2.0.exe (Wagnardsoft Tools) enable it and restart

or 

find ID: open device manager right click your GPU properties and click on events tab

looks like this:

HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Enum\PCI\VEN_10DE&DEV_1E84&SUBSYS_139E10DE&REV_A1\4&3aaa5e18&0&0008\Device Parameters\Interrupt Management\MessageSignaledInterruptProperties

find in regedit and set MSISupported to 1 then restart


~~~~~~~~~~~~~~~~~~~~~~~~~
