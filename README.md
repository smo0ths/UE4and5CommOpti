Updated 7/20/2018

*Post Scriptum works with this aswell

Always testing stuff contact me twitch.tv/smoothschannel or discord

r.OneFrameThreadLag=0 ; lowers input delay test yourself default is 1 

Open Engine.ini and copy paste configs under code:

Press: Windows key + R       
Copy/Paste: %localappdata%/Squad/Saved/Config/WindowsNoEditor/Engine.ini 
Copy/Paste: %localappdata%/PostScriptum/Saved/Config/WindowsNoEditor/Engine.ini 

\\\\\\\\\\\\\\\\\\\\\\\

Max FPS paste this: 

[Core.Log]
Global=all off
LogEasyAntiCheatServer=all off

[Audio]
MaxChannels=64

[SystemSettings]
r.SkeletalMeshLODBias=1
r.ViewDistanceScale=0.8
r.MipMapLODBias=0
r.LightFunctionQuality=0
r.ShadowQuality=0
r.Shadow.CSM.MaxCascades=1
r.Shadow.MaxResolution=512
r.Shadow.MaxCSMResolution=512
r.Shadow.RadiusThreshold=0.06
r.Shadow.DistanceScale=0.6
r.Shadow.CSM.TransitionScale=0
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.VolumetricFog=0
r.VolumetricFog.GridPixelSize=0
r.VolumetricFog.GridSizeZ=0
r.AllowLandscapeShadows=0
r.LightMaxDrawDistanceScale=0
r.MotionBlurQuality=0
r.DepthOfFieldQuality=0
r.RenderTargetPoolMin=300 ; lowest is 200 before no deallocation test yourself
r.LensFlareQuality=0
r.SceneColorFringeQuality=0
r.EyeAdaptationQuality=0
r.BloomQuality=0
r.FastBlurThreshold=0
r.Upscale.Quality=0
r.Tonemapper.GrainQuantization=0
r.LightShaftQuality=0
r.Filter.SizeScale=1
r.Tonemapper.Quality=2
r.Streaming.MipBias=2
r.MaxAnisotropy=0
r.Streaming.LimitPoolSizeToVRAM=0
r.Streaming.PoolSize=1000
r.Streaming.MaxEffectiveScreenSize=0 ; 1 gains fps but some textures are gone
r.TranslucencyLightingVolumeDim=8
r.RefractionQuality=0
r.SSR.Quality=0
r.SceneColorFormat=2 ; 4 for taa/aa no flicker
r.DetailMode=0
r.TranslucencyVolumeBlur=0
r.MaterialQualityLevel=0
r.SSS.Scale=0
r.SSS.SampleSet=0
r.SSS.Quality=0
r.SSS.HalfRes=1
r.EmitterSpawnRateScale=0
r.ParticleMinTimeBetweenTicks=16
r.ParticleLightQuality=0
foliage.DensityScale=0.6
grass.DensityScale=0.6
grass.MaxUpdateFrequency=10
t.MaxFPS=400
r.ReflectionEnvironment=0 ; 1 for txaa/aa no flicker
r.TiledDeferredShading=0
r.TiledDeferredShading.MinimumCount=0
r.StaticMeshLODDistanceScale=0.25
r.VirtualTexture=0
r.EarlyZPass=0
r.EarlyZPassMovable=0
r.HZBOcclusion=0
r.TranslucentLightingVolume=0
r.DoTiledReflections=0
r.OptimizeForUAVPerformance=1 ; set to 0 for GPU memory savings test yourself 
r.CompileShadersForDevelopment=0
r.MinTimeBetweenTicks=16         


\\\\\\\\\\\\\\\\\\\\\\\


My squad and post scriptum high/fps config paste this: 

[Core.Log]
Global=all off
LogEasyAntiCheatServer=all off

[Audio]
MaxChannels=128

[SystemSettings]
r.SkeletalMeshLODBias=0
r.ViewDistanceScale=0.8
r.MipMapLODBias=0
r.LightFunctionQuality=1
r.ShadowQuality=3
r.Shadow.CSM.MaxCascades=2
r.Shadow.MaxResolution=1024
r.Shadow.MaxCSMResolution=2048
r.Shadow.RadiusThreshold=0.03
r.Shadow.DistanceScale=0.4
r.Shadow.CSM.TransitionScale=1.0
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.VolumetricFog=0
r.VolumetricFog.GridPixelSize=0
r.VolumetricFog.GridSizeZ=0
r.AllowLandscapeShadows=0
r.LightMaxDrawDistanceScale=0
r.MotionBlurQuality=0
r.AmbientOcclusionMipLevelFactor=0.5
r.AmbientOcclusionMaxQuality=100
r.AmbientOcclusionLevels=3
r.AmbientOcclusionRadiusScale=0.5
r.DepthOfFieldQuality=0
r.RenderTargetPoolMin=400
r.LensFlareQuality=0
r.SceneColorFringeQuality=0
r.EyeAdaptationQuality=0
r.BloomQuality=0
r.FastBlurThreshold=0
r.Upscale.Quality=3
r.Tonemapper.GrainQuantization=1
r.LightShaftQuality=1
r.Filter.SizeScale=1
r.Tonemapper.Quality=2
r.Streaming.MipBias=0
r.MaxAnisotropy=16
r.Streaming.LimitPoolSizeToVRAM=0
r.Streaming.PoolSize=3000
r.Streaming.MaxEffectiveScreenSize=0
r.TranslucencyLightingVolumeDim=8
r.RefractionQuality=1
r.SSR.Quality=0
r.SceneColorFormat=3
r.DetailMode=2
r.TranslucencyVolumeBlur=0
r.MaterialQualityLevel=1
r.SSS.Scale=0
r.SSS.SampleSet=0
r.SSS.Quality=0
r.SSS.HalfRes=1
r.EmitterSpawnRateScale=1.0
r.ParticleMinTimeBetweenTicks=16
r.ParticleLightQuality=1
foliage.DensityScale=0.6
grass.DensityScale=0.6
grass.MaxUpdateFrequency=10
bSmoothFrameRate=0
s.AsyncLoadingThreadEnabled=1
t.MaxFPS=400
r.VSync=0
r.ReflectionEnvironment=1
r.HalfResReflections=1
r.TiledDeferredShading=1
r.TiledDeferredShading.MinimumCount=0
r.TranslucentLightingVolume=1
r.MinTimeBetweenTicks=16
r.GBufferFormat=3
r.VirtualTexture=1
r.VirtualTextureReducedMemory=1
r.OneFrameThreadLag=0
r.EarlyZPass=2
r.EarlyZPassOnlyMaterialMasking=1
r.HZBOcclusion=1
r.OptimizeForUAVPerformance=1
r.CompileShadersForDevelopment=0
r.SceneColorFringe.Max=0.45
r.LightShaftDownSampleFactor=4
r.SeparateTranslucency=1
r.Tonemapper.Sharpen=0
r.TextureStreaming=1
r.Streaming.HLODStrategy=0
r.SSR.MaxRoughness=0.1
r.DefaultFeature.AmbientOcclusionStaticFraction=0
r.AmbientOcclusion.FadeRadiusScale=0.5


\\\\\\\\\\\\\\\\\\\\\\\


For NVIDIA users in control panel change:

Maximum pre-rendered frames: 1  (test 2 3 4 yourself, lowest is said to have less input lag)
Multi/mixed gpu accel: Single display performance mode
Power management mode: Prefer max performance
Preferred refresh rate: Highest available
Texture filtering anisotropic sample optimization: On
Texture filtering quality: High performance
Vertical sync: Off


\\\\\\\\\\\\\\\\\\\\\\\


Max/Ultra raw settings for reference: 

;ViewDistanceQuality

r.SkeletalMeshLODBias=-1
r.ViewDistanceScale=10.0
r.MipMapLODBias=-1     

;ShadowQuality

r.LightFunctionQuality=1
r.ShadowQuality=5
r.Shadow.CSM.MaxCascades=10
r.Shadow.MaxResolution=4096
r.Shadow.MaxCSMResolution=4096
r.Shadow.RadiusThreshold=0.03
r.Shadow.DistanceScale=1.0
r.Shadow.CSM.TransitionScale=1.0
r.DistanceFieldShadowing=1
r.DistanceFieldAO=1
r.VolumetricFog=1
r.VolumetricFog.GridPixelSize=4
r.VolumetricFog.GridSizeZ=128
r.AllowLandscapeShadows=1        

;PostProcessQuality

r.MotionBlurQuality=4
r.AmbientOcclusionMipLevelFactor=0.4
r.AmbientOcclusionMaxQuality=100
r.AmbientOcclusionLevels=-1
r.AmbientOcclusionRadiusScale=1.0
r.DepthOfFieldQuality=4
r.RenderTargetPoolMin=1000
r.LensFlareQuality=3
r.SceneColorFringeQuality=1
r.EyeAdaptationQuality=2
r.BloomQuality=5
r.FastBlurThreshold=100
r.Upscale.Quality=3
r.Tonemapper.GrainQuantization=1
r.LightShaftQuality=1
r.Filter.SizeScale=1
r.Tonemapper.Quality=5

;TextureQuality

r.Streaming.MipBias=0
r.MaxAnisotropy=16        
r.Streaming.LimitPoolSizeToVRAM=0
r.Streaming.PoolSize=3000
r.Streaming.MaxEffectiveScreenSize=0

;EffectsQuality

r.TranslucencyLightingVolumeDim=64
r.RefractionQuality=2
r.SSR.Quality=4
r.SceneColorFormat=4
r.DetailMode=2
r.TranslucencyVolumeBlur=1
r.MaterialQualityLevel=1      
r.SSS.Scale=1
r.SSS.SampleSet=2
r.SSS.Quality=1
r.SSS.HalfRes=0
r.EmitterSpawnRateScale=1.0
r.ParticleLightQuality=2
r.MinTimeBetweenTicks=8
r.ParticleMinTimeBetweenTicks=16        

;FoliageQuality

foliage.DensityScale=1.0
grass.DensityScale=1.0
grass.MaxUpdateFrequency=30       

;Extra
t.MaxFPS=400
