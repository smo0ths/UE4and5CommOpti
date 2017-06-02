# SquadOpti
This is my attempts at helping optimize the game. I'll update this thread as time goes on and i learn more about the engine. I just want everyone to have the best fps they can without messing with the game and helping devs out with the game, thanks.

Download: UE4PakUnpacker.exe (941,568 bytes) (you need to find the download link from google)
Unpack: pakchunk0-WindowsNoEditor.pak
Found in:
Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Squad/Content/Paks/

Now you can open up DefaultEngine.ini:
Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Squad/Config/DefaultEngine.ini

Find and Edit these commands are already in the file:
MaxChannels=64  (Faster cpu's use 96 or default 128)
Turn off logging: Find: [Core.Log] Add this: Global=off (remove all blahblah=log stuff)
r.GBufferFormat=0
r.SeparateTranslucency=0
r.EarlyZPass=0

Find: Steam\steamapps\common\Squad\Squad\Config\DefaultEngine.ini
Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Squad/Config/DefaultEngine.ini

Copy and Paste under [systemSettings]

; VIEWDISTANCE
r.SkeletalMeshLODBias=1.5
r.ViewDistanceScale=0.8
r.MipMapLODBias=0
; SHADOW  
r.LightFunctionQuality=0
r.ShadowQuality=0
r.Shadow.CSM.MaxCascades=0
r.Shadow.MaxResolution=0
r.Shadow.RadiusThreshold=0
r.Shadow.DistanceScale=0
r.Shadow.CSM.TransitionScale=0
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.AllowLandscapeShadows=0
; POSTPROCESS
r.MotionBlurQuality=0
r.AmbientOcclusionMipLevelFactor=0
r.AmbientOcclusionMaxQuality=0
r.AmbientOcclusionLevels=0
r.AmbientOcclusionRadiusScale=0
r.DepthOfFieldQuality=0
r.RenderTargetPoolMin=300
r.LensFlareQuality=0
r.SceneColorFringeQuality=0
r.EyeAdaptationQuality=0
r.BloomQuality=0
r.FastBlurThreshold=0
r.Upscale.Quality=0
r.Tonemapper.GrainQuantization=0
r.LightShaftQuality=0
r.Filter.SizeScale=0
r.Tonemapper.Quality=2
; TEXTURE
r.Streaming.MipBias=2  
r.MaxAnisotropy=0
;r.Streaming.LimitPoolSizeToVRAM=0 
;r.Streaming.PoolSize=1024 
; EFFECTS
r.TranslucencyLightingVolumeDim=8
r.TranslucencyLightingVolumeInnerDistance=16  
r.TranslucencyLightingVolumeOuterDistance=16 
r.RefractionQuality=0
r.SSR.Quality=0
r.SceneColorFormat=2  
r.DetailMode=0
r.TranslucencyVolumeBlur=0
r.MaterialQualityLevel=0
r.SSS.Scale=0
r.SSS.SampleSet=0
r.SSS.Quality=0
r.SSS.HalfRes=1
r.EmitterSpawnRateScale=0
r.DefaultFeature.AutoExposure=0
r.ParticleMinTimeBetweenTicks=33
r.ParticleLightQuality=0
; FOLIAGE
foliage.DensityScale=0.6
grass.DensityScale=0.6
grass.MaxUpdateFrequency=10
; EXTRA
r.ReflectionEnvironment=0  
r.TiledDeferredShading=0  
r.Decal.FadeScreenSizeMult=0
r.SkeletalMeshLODRadiusScale=0.25
r.VirtualTexture=0
r.RHICmdBypass=0
t.MaxFPS=400
; END


Set in-game graphics settings to medium to get AA to work in game on/off.
Updated for Squad v9.4

The above is for max fps, below for more configs and stuff.
Bloom/eye adapt/lensflare on/off works in game now threw GameUserSettings.ini
Set sg.PostProcessQuality=3 in GameUserSettings.ini to make sure you are getting highest quality SSAO when set on.

My config:

; VIEWDISTANCE
r.SkeletalMeshLODBias=-1
r.ViewDistanceScale=0.8
r.MipMapLODBias=-1
; SHADOW
;r.LightFunctionQuality=
;r.ShadowQuality=
;r.Shadow.CSM.MaxCascades=
;r.Shadow.MaxResolution=
;r.Shadow.RadiusThreshold=
;r.Shadow.DistanceScale=
;r.Shadow.CSM.TransitionScale=
;r.DistanceFieldShadowing=
;r.DistanceFieldAO=
;r.AllowLandscapeShadows=
; POSTPROCESS
r.MotionBlurQuality=0
;r.AmbientOcclusionMipLevelFactor=
;r.AmbientOcclusionMaxQuality=
;r.AmbientOcclusionLevels=
;r.AmbientOcclusionRadiusScale=
r.DepthOfFieldQuality=0
r.RenderTargetPoolMin=1000
r.LensFlareQuality=2
r.SceneColorFringeQuality=1
r.EyeAdaptationQuality=0
r.BloomQuality=1
r.FastBlurThreshold=0
r.Upscale.Quality=0
r.Tonemapper.GrainQuantization=0
r.LightShaftQuality=0
r.Filter.SizeScale=0
r.Tonemapper.Quality=2
; TEXTURE
r.Streaming.MipBias=0
r.MaxAnisotropy=16
r.Streaming.LimitPoolSizeToVRAM=0
r.Streaming.PoolSize=3000
; EFFECTS
r.TranslucencyLightingVolumeDim=24
r.TranslucencyLightingVolumeInnerDistance=24
r.TranslucencyLightingVolumeOuterDistance=24
r.RefractionQuality=0
r.SSR.Quality=0
r.SceneColorFormat=4
r.DetailMode=0
r.TranslucencyVolumeBlur=0
r.MaterialQualityLevel=1
r.SSS.Scale=0
r.SSS.SampleSet=0
r.SSS.Quality=0
r.SSS.HalfRes=1
r.EmitterSpawnRateScale=0.75
;r.DefaultFeature.AutoExposure=0
r.ParticleMinTimeBetweenTicks=16
r.ParticleLightQuality=1
; FOLIAGE
foliage.DensityScale=0.6
grass.DensityScale=0.6
grass.MaxUpdateFrequency=10
; EXTRA
r.SceneColorFringe.Max=0.1
r.Decal.FadeScreenSizeMult=0.25
t.MaxFPS=400
;r.ReflectionEnvironment=0
r.VirtualTexture=0
r.TiledDeferredShading=0
r.TiledDeferredShading.MinimumCount=0
r.TiledReflectionEnvironmentMinimumCount=0
r.RHICmdBypass=0
r.AmbientOcclusionSampleSetQuality=0
; END

Change shadows in game:

Edit DefaultScalability.ini and BaseScalability.ini: ShadowQuality @ 0 @ 1 @ 2 @ 3 to whatever you like and you can change them in game
Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Squad/Config/DefaultScalability.ini
Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Engine/Config/BaseScalability.ini

i use this....

[ShadowQuality@0]
r.LightFunctionQuality=1
r.ShadowQuality=0
r.Shadow.CSM.MaxCascades=0
r.Shadow.MaxResolution=0
r.Shadow.RadiusThreshold=0
r.Shadow.DistanceScale=0
r.Shadow.CSM.TransitionScale=0
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.AllowLandscapeShadows=0

[ShadowQuality@1]
r.LightFunctionQuality=1
r.ShadowQuality=3
r.Shadow.CSM.MaxCascades=1
r.Shadow.MaxResolution=1024
r.Shadow.RadiusThreshold=0.03
r.Shadow.DistanceScale=0.35
r.Shadow.CSM.TransitionScale=0.75
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.AllowLandscapeShadows=0

[ShadowQuality@2]
r.LightFunctionQuality=1
r.ShadowQuality=3
r.Shadow.CSM.MaxCascades=2
r.Shadow.MaxResolution=2048
r.Shadow.RadiusThreshold=0.03
r.Shadow.DistanceScale=0.35
r.Shadow.CSM.TransitionScale=0.75
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.AllowLandscapeShadows=0

[ShadowQuality@3]
r.LightFunctionQuality=1
r.ShadowQuality=3
r.Shadow.CSM.MaxCascades=2
r.Shadow.MaxResolution=4096
r.Shadow.RadiusThreshold=0.03
r.Shadow.DistanceScale=0.35
r.Shadow.CSM.TransitionScale=0.75
r.DistanceFieldShadowing=0
r.DistanceFieldAO=0
r.AllowLandscapeShadows=0

Skip intro video:

Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Squad/Config/DefaultGame.ini
Add a ; in front of the command below:
;+StartupMovies=squad_intro_movie

Load up any map to test:

Windows key + R: %SystemDrive%/Program Files (x86)/Steam/steamapps/common/Squad/Squad/Config/DefaultGame.ini
Change: MainMenuMap=/Game/Maps/EntryMap
Example: MainMenuMap=/Game/Maps/BASRAH_CITY/Albasrah_invasion_v1

Launch options:  
-sm4 (same as -d3d10, test yourself)

For NVIDIA users in control panel change:

Maximum pre-rendered frames: 1  (test 2 3 4 yourself, lowest is said to have less input lag)
Multi/mixed gpu accel: Single display performance mode
Power management mode: Prefer max performance
Preferred refresh rate: Highest available
Texture filtering anisotropic sample optimization: On
Texture filtering quality: High performance
Vertical sync: Off