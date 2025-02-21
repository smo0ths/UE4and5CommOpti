## updated 2/20/2025 ✂ 📋 🌀 :ramen: v0.8.8

### for ue4 and ue5* games for reference/customization/optimization/learning

#### my config is trying to be quality and perform well for any ue4/5 game, it might not be perfectly optimal for a specific game

#### always testing stuff contact me [smoothschannel](https://twitch.tv/smoothschannel) or [discord](https://discord.gg/tdzt7qsx8m)

#### [installing and optimizing nvidia drivers here](https://github.com/smo0ths/installing-and-optimizing-new-nvidia-drivers-on-windows-11-gaming-pc)

#### check 🔴 options for more fps (left to right, performance to quality)

#### 2560x1440 use 🔴 58%,67%,70% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

#### 3328x1872 use 🔴 50%,58%,67% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

#### 3840x2160 use 🔴 33%,50%,58%,67% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

## open engine.ini and copy pasta %localappdata%

#### 1. add config 2. open game and adjust settings (config doesn't touch lods like view distance so set low or higher) 3. restart game

#### or repak.bat method if it works (zzz_inimods\engine\config\windows\windowsengine.ini)

```python
[core.log]
global=off;
logtelemetry=all off;

[crashreportclient]
ballowtobecontacted=0;
bisallowedtoclosewithoutsending=1;
bsendlogfile=0;
cansendwhenuifailedtoinitialize=0;
datarouterurl="about:blank";
uiinitretrycount=0;

[/script/engine.engine]
bpauseonlossoffocus=0;
bsmoothframerate=0;
busefixedframerate=0;

[texturestreaming]
poolsizevrampercentage=70; 🔴 50 to lower vram usage 🔵 texturepool cache

[consolevariables]

; direct3d
d3d12.texturepoolonlyaccountstreamabletexture=1; 🔵 newer
r.d3d.forcedxc=1; 🔵 dxc shader compiler instead of fxc
r.d3d12.allowshadermodel6=1; 🔵 sm6 support
r.d3d12.shadowdepth32bit=0; 🔵 16bit shadow depth

; scaling
r.antialiasingmethod=0; 🔵 0 off 1 fxaa 2 taa 3 msaa 4 tsr
r.customdepthtemporalaajitter=0;
r.dynamicres.operationmode=0;
r.fidelityfx.fsr.enabled=0; 🔵 fsr
r.fidelityfx.fsr2.enabled=0; 🔵 fsr2
r.fidelityfx.fsr3.enabled=0; 🔵 fsr3
r.fxaa.quality=0;
r.ngx.dlss.autoexposure=1;
r.ngx.dlss.dilatemotionvectors=1;
r.ngx.dlss.enable=1; 🔵 dlss
r.ngx.dlss.prefernissharpen=0;
r.ngx.dlss.quality.auto=0;
r.ngx.dlss.reflections.temporalaa=0;
r.ngx.dlss.sharpness=0;
r.ngx.dlss.waterreflections.temporalaa=0;
r.nis.enable=0; 🔵 nis
r.nis.sharpness=0;
r.postprocessaaquality=0; 🔵 0 off 1,2 fxaa 3,4,5,6 taa
r.secondaryscreenpercentage.gameviewport=0;
r.ssr.experimentaldenoiser=0;
r.temporalaa.quality=0;
r.temporalaa.upsampling=1; 🔴 0 for performance 🔵 taau
r.temporalaasamples=8;
r.tsr.16bitvalu.amd=1;
r.tsr.16bitvalu.intel=1;
r.tsr.16bitvalu.nvidia=1;
r.tsr.16bitvalu=0;
r.vrs.enable=0;
r.vrs.enableimage=0;
r.vrs.enablesoftware=0;
r.xess.enabled=0; 🔵 xess
t.streamline.reflex.auto=1;
t.streamline.reflex.enable=1; 🔵 reflex amd frame gen not supported
t.streamline.reflex.mode=2;

; async
fx.niagara.asyncgputrace.hwraytraceenabled=0;
r.bloom.asynccompute=1;
r.d3d12.allowasynccompute=1;
r.dfshadowasynccompute=1;
r.lumen.asynccompute=1;
r.lumen.diffuseindirect.asynccompute=1;
r.lumen.reflections.asynccompute=1;
r.lumenscene.lighting.asynccompute=1;
r.nanite.asyncrasterization.shadowdepths=0;
r.nanite.asyncrasterization=1;
r.nanite.streaming.asynccompute=1;
r.scenedepthhzbasynccompute=1;
r.skyatmosphereasynccompute=1;
r.volumetricrendertarget.preferasynccompute=1;
r.vulkan.allowasynccompute=1;

; shaders
r.shaders.removedeadcode=1;
r.shaders.removeunusedinterpolators=1;

; nanite
r.gpuscene.parallelupdate=1;
r.nanite.streaming.imposters=0;
r.nanite.viewmeshlodbias.min=-2;
r.nanite.viewmeshlodbias.offset=0;

; texture
r.anisotropicmaterials=1; 🔴 0 for performance
r.landscapelodbias=0; 🔴 1 for performance
r.materialqualitylevel=1; 🔴 0,2 for performance
r.maxanisotropy=16; 🔴 0,4,8 for performance
r.optimizedwpo=1;
r.streaming.amortizecputogpucopy=0;
r.streaming.boost=1;
r.streaming.fullyloadusedtextures=0;
r.streaming.hiddenprimitivescale=0.5; 🔴 0.5 for performance
r.streaming.limitpoolsizetovram=1;
r.streaming.maxeffectivescreensize=0;
r.streaming.maxnumtexturestostreamperframe=0;
r.streaming.mipbias=0; 🔴 1 for performance
r.streaming.poolsize.vrampercentageclamp=1024;
r.streaming.poolsize=1000;
r.streaming.poolsizeformeshes=-1;
r.streaming.useallmips=0;
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=1;
r.supportmateriallayers=1; 🔴 0 for performance
r.tessellationadaptivepixelspertriangle=999999; 🔴 999999,48 for performance
r.texturestreaming=1;
r.virtualtexture=0;
r.virtualtexturedlightmaps=0;
r.virtualtexturereducedmemory=0;
r.virtualtextures=1;
r.vt.anisotropicfiltering=1;
r.vt.maxanisotropy=8; 🔴 0,4 for performance
r.vt.maxreleasedperframe=0;
r.vt.maxtilesproducedperframe=96;
r.vt.maxuploadsperframe.streaming=48;
r.vt.maxuploadsperframe=16;

; latency
d3d12.maximumframelatency=1; 🔵 frame latency
r.d3d11.useallowtearing=1; 🔵 dxgi flip mode
r.d3d12.useallowtearing=1; 🔵 dxgi flip mode
r.gtsynctype=0;
r.vsync=0;
rhi.maximumframelatency=1; 🔵 frame latency
t.maxfps=0;
t.overridefps=0;

; occlusion system
r.hzbocclusion=1;
r.numbufferedocclusionqueries=2; 🔵 frames to buffer queries

; debug
r.d3d12.gpucrashdebuggingmode=0;
r.detectandwarnofbaddrivers=0;
r.gpucrash.collectionenable=0;
r.ngx.loglevel=0;
r.vsyncinformationinsights=0;

; reflection
r.chaos.reflectioncapturestaticsceneonly=1;
r.reflectioncaptureresolution=128; 🔴 128 for performance
r.reflectioncapturesupersamplefactor=1;

; refraction
r.refraction.blur.temporalaa=1; 🔵 temporal filtering
r.refractionquality=2; 🔴 0,1 for performance

; screen space global illumination
r.ssgi.enable=0; 🔴 0 for performance

; screen space reflections
r.ssr.halfresscenecolor=1; 🔴 1 for performance
r.ssr.quality=2; 🔴 0,2 for performance

; sub surface scattering
r.sss.burley.quality=0; 🔴 0 for performance
r.sss.checkerboard=2; 🔴 1 for performance
r.sss.halfres=0; 🔴 1 for performance
r.subsurfacescattering=1; 🔴 0 for performance

; physics
p.animdynamics=1; 🔴 0 for performance
p.animdynamicswind=1; 🔴 0 for performance
p.rigidbodynode=1; 🔴 0 for performance

; particle
fx.niagara.qualitylevel=3; 🔴 0,1,2 for performance
fx.niagaraallowruntimescalabilitychanges=1;
r.emitterspawnratescale=1; 🔴 0.125,0.25,0.5 for performance
r.particlelightquality=2; 🔴 0,1 for performance

; screen space ambient occlusion
r.ambientocclusionlevels=-1; 🔴 0,1 for performance
r.ambientocclusionmaxquality=100;
r.ambientocclusionstaticfraction=-1; 🔴 0 for performance

; distance field ambient occlusion
r.aoquality=2; 🔴 0 for performance

; post process
r.bloom.screenpercentage=50;
r.bloomquality=4; 🔴 0 for performance
r.blurgbuffer=0;
r.depthoffieldquality=0; 🔴 0,1 for performance
r.dof.gather.accumulatorquality=0;
r.dof.gather.enablebokehsettings=0;
r.dof.gather.postfiltermethod=1;
r.dof.gather.ringcount=3;
r.dof.kernel.maxbackgroundradius=0.012;
r.dof.kernel.maxforegroundradius=0.012;
r.dof.recombine.quality=0;
r.dof.scatter.backgroundcompositing=0;
r.dof.scatter.enablebokehsettings=0;
r.dof.scatter.foregroundcompositing=0;
r.dof.scatter.maxspriteratio=0.04;
r.dof.temporalaaquality=0;
r.filmgrain=0;
r.filter.loopmode=0; 🔴 0 for performance
r.filter.sizescale=1;
r.motionblurquality=0;
r.postprocessing.prefercompute=1;
r.scenecolorformat=4; 🔴 2,3 for performance
r.scenecolorfringe.max=0;
r.separatetranslucencyautodownsample=1;
r.separatetranslucencyscreenpercentage=100;
r.tonemapper.grainquantization=0;
r.tonemapper.quality=2;
r.tonemapper.sharpen=0;
r.upscale.quality=3; 🔴 1,2 for performance

; light
r.lightmaxdrawdistancescale=1; 🔴 0.6 for performance
r.minscreenradiusforlights=0.03; 🔴 0.06,0.04 for performance

; hair
r.hairstrands.composeaftertranslucency=0;
r.hairstrands.deepshadow.supersampling=0;
r.hairstrands.enable=1; 🔴 0 for performance
r.hairstrands.interpolation.usesingleguide=1; 🔴 1 for performance
r.hairstrands.minlod=0;
r.hairstrands.rasterizationscale=0.5;
r.hairstrands.scatterscenelighting=1;
r.hairstrands.shadow.castshadowwhennonvisible=0;
r.hairstrands.simulation=1;
r.hairstrands.skyao.samplecount=4;
r.hairstrands.skyao=0; 🔴 0 for performance
r.hairstrands.skylighting.integrationtype=2;
r.hairstrands.skylighting.samplecount=16;
r.hairstrands.skylighting.screentraceocclusion=0; 🔵 experiemental
r.hairstrands.skylighting=1;
r.hairstrands.usecardsinsteadofstrands=0; 🔴 1 for performance
r.hairstrands.velocityrasterizationscale=1;
r.hairstrands.visibility.msaa.sampleperpixel=4; 🔴 1,2 for performance
r.hairstrands.visibility.ppll=0; 🔴 0 for performance
r.hairstrands.voxelization.voxelsizeinpixel=0.3;
r.hairstrands.voxelization=0; 🔴 0 for performance

; rtx switch
r.lumen.hardwareraytracing=0;
r.raytracing=0;

; rtx 1
r.heterogeneousvolumes.hardwareraytracing=0;
r.lumen.hardwareraytracing.inline=0;
r.lumen.hardwareraytracing.lightingmode=0; 🔴 0 for performance
r.lumen.radiancecache.hardwareraytracing=1;
r.lumen.reflections.hardwareraytracing=1;
r.lumen.screenprobegather.hardwareraytracing=1; 🔵 diffuse indirect
r.lumen.screenprobegather.shortrangeao.hardwareraytracing=0;
r.lumen.translucencyvolume.hardwareraytracing=1;
r.lumenscene.directlighting.hardwareraytracing=1;
r.lumenscene.radiosity.hardwareraytracing=1;
r.manylights.hardwareraytracing=1;

; rtx 2
r.hairstrands.raytracing=0;
r.ngx.dlss.denoisermode=0; 🔵 ray reconstruction needs dlssd
r.pathtracing=0;
r.raytracing.excludedecals=1;
r.raytracing.excludesky=1;
r.raytracing.excludetranslucent=1;
r.raytracing.geometry.hierarchicalinstancedstaticmesh=0;
r.raytracing.geometry.instancedstaticmeshes=0;
r.raytracing.geometry.landscape=0;
r.raytracing.geometry.landscapegrass=0;
r.raytracing.geometry.niagarameshes=0;
r.raytracing.geometry.niagararibbons=0;
r.raytracing.geometry.niagarasprites=0;
r.raytracing.geometry.proceduralmeshes=0;
r.raytracing.geometry.skeletalmeshes=0;
r.raytracing.geometry.splinemeshes=0;
r.raytracing.geometry.staticmeshes=0;
r.raytracing.globalillumination=0;
r.raytracing.reflections.experimentaldeferred=0;
r.raytracing.reflections.hybrid=0;
r.raytracing.reflections=0;
r.raytracing.shadows.enablehairvoxel=0;
r.raytracing.shadows.enablematerials=0;
r.raytracing.shadows.enabletwosidedgeometry=0;
r.raytracing.shadows.maxbatchsize=8;
r.raytracing.shadows=0;
r.raytracing.skylight=0;
r.raytracing.translucency=0;
r.volumetricfog.injectraytracedlights.locallights=0;
r.volumetricfog.injectraytracedlights=0;

; lumen 1
r.lumen.diffuseindirect.allow=1; 🔵 lumen global illumination
r.lumen.reflections.allow=1; 🔵 lumen reflections
r.lumen.reflections.tracemeshsdfs=1;
r.lumen.screenprobegather.tracemeshsdfs=1;
r.lumen.tracemeshsdfs.allow=1;
r.lumen.tracemeshsdfs=0; 🔴 0 for performance

; lumen 2
r.distancefields.supportevenifhardwareraytracingsupported=0; 🔵 rtx df
r.gbufferdiffusesampleocclusion=1; 🔵 bent normal maps
r.lumen.diffuseindirect.ssao=0;
r.lumen.radiancecache.numframestokeepcachedprobes=8;
r.lumen.reflections.bilateralfilter.numsamples=4;
r.lumen.reflections.bilateralfilter.spatialkernelradius=0.002;
r.lumen.reflections.bilateralfilter=1;
r.lumen.reflections.downsamplefactor=1; 🔴 2 for performance
r.lumen.reflections.maxroughnesstotrace=1;
r.lumen.reflections.maxroughnesstotraceforfoliage=1;
r.lumen.reflections.smoothbias=1;
r.lumen.reflections.radiancecache=1; 🔵 radiance cache
r.lumen.reflections.screenspacereconstruction.tonemapstrength=0;
r.lumen.reflections.screenspacereconstruction=1; 🔵 reconstruction
r.lumen.reflections.specularindirectbuffer32bit=0; 🔴 1 for performance
r.lumen.reflections.temporal=1; 🔵 temporal filtering
r.lumen.restirgather=0;
r.lumen.samplefog=0;
r.lumen.screenprobegather.downsamplefactor=8; 🔴 16,32 for performance 🔵 light noise
r.lumen.screenprobegather.materialao=1;
r.lumen.screenprobegather.radiancecache.probeatlasresolutioninprobes=128;
r.lumen.screenprobegather.radiancecache=1; 🔵 persistent world space radiance cache
r.lumen.screenprobegather.screenspacebentnormal=1; 🔵 bent normal maps, changed to shortrangeao
r.lumen.screenprobegather.screentraces=1;
r.lumen.screenprobegather.shortrangeao.applyduringintegration=0;
r.lumen.screenprobegather.shortrangeao=1;
r.lumen.screenprobegather.stochasticinterpolation=1; 🔴 1 for performance
r.lumen.screenprobegather.temporal=1; 🔵 temporal filtering
r.lumen.screenprobegather.tracingoctahedronresolution=8;
r.lumen.screenprobegather.twosidedfoliagebackfacediffuse=1;
r.lumen.translucencyreflections.frontlayer.allow=1; 🔴 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=1; 🔴 0 for performance
r.lumen.translucencyvolume.enable=1;
r.lumen.translucencyvolume.radiancecache.probeatlasresolutioninprobes=80;
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0;
r.lumenscene.farfield.maxtracedistance=100000;
r.lumenscene.farfield=0;
r.lumenscene.radiosity.probeocclusion=0; 🔴 0 for performance

; shadow
r.allowlandscapeshadows=1; 🔴 0 for performance
r.dffullresolution=0; 🔴 0 for performance
r.dfshadowquality=2; 🔴 1,2 for performance
r.shadow.csm.maxcascades=2; 🔴 1,2,4 for performance
r.shadow.csmshadowdistancefadeoutmultiplier=1;
r.shadow.distancescale=1; 🔴 0.7 for performance
r.shadow.forcesinglesampleshadowingfromstationary=0; 🔴 1 for performance
r.shadow.maxcsmresolution=2048; 🔴 512,1024 for performance
r.shadow.maxresolution=2048; 🔴 512,1024 for performance
r.shadow.nanitelodbias=1; 🔴 1 for performance
r.shadow.radiusthreshold=0.03; 🔴 0.06,0.05,0.04 for performance
r.shadowquality=4; 🔴 3,4 for performance
r.translucencylightingvolumedim=64; 🔴 32,48 for performance
r.translucencyvolumeblur=1; 🔴 0 for performance

; virtual shadow maps
r.shadow.virtual.nonnanite.includeincoarsepages=0; 🔴 0 for performance
r.shadow.virtual.onepassprojection.maxlightsperpixel=16; 🔴 8 for performance
r.shadow.virtual.smrt.raycountdirectional=4; 🔴 2,4 for performance
r.shadow.virtual.smrt.raycountlocal=4; 🔴 2,4 for performance
r.shadow.virtual.smrt.samplesperraydirectional=2; 🔴 1,2 for performance
r.shadow.virtual.smrt.samplesperrayhair=1;
r.shadow.virtual.smrt.samplesperraylocal=2; 🔴 1,2 for performance
r.shadow.virtual.subsurfaceshadowmode=1;
r.shadow.virtual.translucentquality=0; 🔴 0 for performance

; sky
r.skyatmosphere.fastskylut.samplecountmax=64; 🔴 32,64 for performance
r.skyatmosphere.fastskylut.samplecountmin=1; 🔴 1 for performance
r.skyatmosphere.lut32=0; 🔴 0 for performance
r.skyatmosphere.multiscatteringlut.highquality=0; 🔴 0 for performance
r.skyatmosphere.multiscatteringlut.samplecount=15;
r.skyatmosphere.samplecountmax=64; 🔴 32,64 for performance
r.skyatmosphere.samplecountmin=1; 🔴 1 for performance
r.skyatmosphere.samplelightshadowmap=0; 🔴 0 for performance 🔵 volumetric shadows
r.skyatmosphere.transmittancelut.samplecount=10;
r.skyatmosphere.transmittancelut.usesmallformat=0; 🔴 1 for performance

; clouds
r.volumetriccloud.distancetosamplemaxcount=15;
r.volumetriccloud.enableatmosphericlightssampling=1;
r.volumetriccloud.enabledistantskylightsampling=1;
r.volumetriccloud.enablelocallightssampling=0; 🔴 0 for performance 🔵 experimental
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 🔴 0 for performance 🔵 volumetric shadows
r.volumetriccloud.shadowmap.spatialfiltering=1; 🔵 cloud shadow blur
r.volumetriccloud.shadowmap=1;
r.volumetriccloud.skyao=1;
r.volumetriccloud=1; 🔴 0 for performance

; fog
r.fog=1; 🔵 render fog
r.volumetricfog.conservativedepth=0; 🔵 experimental
r.volumetricfog.depthdistributionscale=32; 🔴 16 for performance
r.volumetricfog.emissive=0;
r.volumetricfog.gridpixelsize=16; 🔴 16 for performance
r.volumetricfog.gridsizez=96; 🔴 64 for performance
r.volumetricfog.historymisssupersamplecount=2; 🔴 2 for performance
r.volumetricfog.jitter=1; 🔵 temporal filtering
r.volumetricfog.temporalreprojection=1;
r.volumetricfog.upsamplejittermultiplier=1; 🔴 0 for performance
r.volumetricfog=1; 🔴 0 for performance

; water
r.water.enableshallowwatersimulation=0; 🔴 0 for performance
r.water.enableunderwaterpostprocess=0; 🔴 0 for performance
r.water.reflections.maxroughnesstotrace=1;
r.water.singlelayer.depthprepass=1;
r.water.singlelayer.distancefieldshadow=1;
r.water.singlelayer.downsamplereflections=1; 🔴 1 for performance
r.water.singlelayer.reflection=1; 🔵 reflection technique
r.water.singlelayer.refractiondownsamplefactor=1; 🔴 1,2 for performance
r.water.singlelayer.rtr=0; 🔴 0 for performance
r.water.singlelayer.shaderssupportdistancefieldshadow=1;
r.water.singlelayer.shaderssupportvsmfiltering=1;
r.water.singlelayer.ssr=0; 🔴 0 for performance
r.water.singlelayer.tiledcomposite=1;
r.water.singlelayer.underwaterfogwhencameraisabovewater=0;
r.water.singlelayer.vsmfiltering=1;
r.water.watermesh.tessfactorbias=0; 🔴 -1 for performance
```

---

## open input.ini and copy pasta %localappdata%

#### or repak.bat method if it works (zzz_inimods\engine\config\windows\windowsinput.ini)

```python
[/script/engine.inputsettings]
baltentertogglesfullscreen=1;
benablemousesmoothing=0;
bf11togglesfullscreen=0;
buttonrepeatdelay=0.1;
bviewaccelerationenabled=0;
doubleclicktime=0.01; 🔵 def 0.1
initialbuttonrepeatdelay=0.1; 🔵 def 0.2
```

---
