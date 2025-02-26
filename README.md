## updated 2/26/2025 ✂ 📋 🌀 :ramen: v0.9.9

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

#### if you get ue4 crash/error set r.raytracing=0; (if you crash after changing command try again without changing anything should not crash again) any further crash is another command in the pipe.

#### or repak.bat method if it works (zzz_inimods\engine\config\windows\windowsengine.ini)

```python
[core.log]
global=off;

[crashreportclient]
ballowtobecontacted=0;
bisallowedtoclosewithoutsending=1;
bsendlogfile=0;
cansendwhenuifailedtoinitialize=0;
datarouterurl="";
uiinitretrycount=0;

[/script/engine.engine]
bpauseonlossoffocus=0;
bsmoothframerate=0;
busefixedframerate=0;

[texturestreaming]
poolsizevrampercentage=70; 🔴 50 to lower vram usage

[consolevariables]
;
; perf
;
r.allowlandscapeshadows=1; 🔴 0 for performance
r.ambientocclusionlevels=-1; 🔴 0,1 for performance
r.ambientocclusionstaticfraction=-1; 🔴 0 for performance
r.anisotropicmaterials=1; 🔴 0 for performance
r.aoquality=2; 🔴 0 for performance
r.bloomquality=4; 🔴 0 for performance
r.capsuleshadows=0; 🔴 0 for performance
r.d3d12.shadowdepth32bit=0; 🔴 0 for performance
r.depthoffieldquality=0; 🔴 0,1 for performance
r.dffullresolution=0; 🔴 0 for performance
r.dfshadowquality=2; 🔴 1,2 for performance
r.emitterspawnratescale=1; 🔴 0.125,0.25,0.5 for performance
r.filter.loopmode=0; 🔴 0 for performance
r.hairstrands.interpolation.usesingleguide=1; 🔴 1 for performance
r.hairstrands.skyao=0; 🔴 0 for performance
r.hairstrands.usecardsinsteadofstrands=0; 🔴 1 for performance
r.hairstrands.visibility.msaa.sampleperpixel=1; 🔴 1,2 for performance
r.hairstrands.visibility.ppll=0; 🔴 0 for performance
r.hairstrands.voxelization=0; 🔴 0 for performance
r.landscapelodbias=0; 🔴 1 for performance
r.lightmaxdrawdistancescale=1; 🔴 0.6 for performance
r.maxanisotropy=16; 🔴 0,4,8 for performance
r.minscreenradiusforlights=0.03; 🔴 0.06,0.04 for performance
r.particlelightquality=1; 🔴 0,1 for performance
r.refractionquality=2; 🔴 0,1 for performance
r.scenecolorformat=3; 🔴 2,3 for performance
r.shadow.cachedshadowscastfrommovableprimitives=0; 🔴 0 for performance
r.shadow.forcesinglesampleshadowingfromstationary=1; 🔴 1 for performance
r.shadow.nanitelodbias=1; 🔴 1 for performance
r.shadow.radiusthreshold=0.04; 🔴 0.06,0.05,0.04 for performance
r.skyatmosphere.fastskylut.samplecountmax=64; 🔴 32 for performance
r.skyatmosphere.fastskylut.samplecountmin=4; 🔴 1 for performance
r.skyatmosphere.lut32=0; 🔴 0 for performance
r.skyatmosphere.multiscatteringlut.highquality=0; 🔴 0 for performance
r.skyatmosphere.samplecountmax=64; 🔴 32 for performance
r.skyatmosphere.samplecountmin=4; 🔴 1 for performance
r.skyatmosphere.samplelightshadowmap=0; 🔴 0 for performance
r.skyatmosphere.transmittancelut.usesmallformat=0; 🔴 1 for performance
r.ssgi.enable=0; 🔴 0 for performance
r.ssr.halfresscenecolor=1; 🔴 1 for performance
r.ssr.quality=2; 🔴 0,2 for performance
r.sss.burley.quality=0; 🔴 0 for performance
r.sss.checkerboard=1; 🔴 1 for performance
r.sss.halfres=1; 🔴 1 for performance
r.streaming.hiddenprimitivescale=0.5; 🔴 0.5 for performance
r.streaming.mipbias=0; 🔴 1 for performance
r.subsurfacescattering=1; 🔴 0 for performance
r.supportmateriallayers=1; 🔴 0 for performance
r.temporalaa.upsampling=1; 🔴 0 for performance
r.tessellationadaptivepixelspertriangle=999999; 🔴 999999,48 for performance
r.translucencylightingvolumedim=48; 🔴 32,48 for performance
r.translucencyvolumeblur=1; 🔴 0 for performance
r.upscale.quality=2; 🔴 1,2 for performance
r.volumetriccloud.enablelocallightssampling=0; 🔴 0 for performance
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 🔴 0 for performance
r.volumetriccloud=1; 🔴 0 for performance
r.volumetricfog.depthdistributionscale=16; 🔴 16 for performance
r.volumetricfog.gridpixelsize=16; 🔴 16 for performance
r.volumetricfog.gridsizez=64; 🔴 64 for performance
r.volumetricfog.historymisssupersamplecount=2; 🔴 2 for performance
r.volumetricfog.upsamplejittermultiplier=0; 🔴 0 for performance
r.volumetricfog=1; 🔴 0 for performance
r.vt.anisotropicfiltering=1; 🔴 0 for performance
r.vt.maxanisotropy=8; 🔴 4 for performance
r.water.enableshallowwatersimulation=0; 🔴 0 for performance
r.water.enableunderwaterpostprocess=0; 🔴 0 for performance
r.water.singlelayer.downsamplereflections=1; 🔴 1 for performance
r.water.singlelayer.reflection=1; 🔴 0 for performance
r.water.singlelayer.refractiondownsamplefactor=1; 🔴 1,2 for performance
r.water.singlelayer.ssr=0; 🔴 0 for performance
r.water.watermesh.tessfactorbias=0; 🔴 -1 for performance
;
; ue5
;
fx.niagara.qualitylevel=2; 🔴 0,1,2 for performance
r.lumen.hardwareraytracing=1; 🔴 0 for performance
r.lumen.reflections.downsamplefactor=1; 🔴 2 for performance
r.lumen.reflections.maxroughnesstotrace=0.4; 🔴 -1,0.4 for performance
r.lumen.reflections.smoothbias=0.4; 🔴 0,0.4 for performance
r.lumen.reflections.specularindirectbuffer32bit=0; 🔴 0 for performance
r.lumen.reflections.tracemeshsdfs=0; 🔴 0 for performance
r.lumen.screenprobegather.downsamplefactor=16; 🔴 16,32 for performance
r.lumen.screenprobegather.stochasticinterpolation=1; 🔴 1 for performance
r.lumen.tracemeshsdfs.allow=1; 🔴 0 for performance
r.lumen.tracemeshsdfs=0; 🔴 0 for performance
r.lumen.translucencyreflections.frontlayer.allow=0; 🔴 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0; 🔴 0 for performance
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0; 🔴 0 for performance
r.lumenscene.farfield.maxtracedistance=100000; 🔴 100000 for performance
r.lumenscene.radiosity.probeocclusion=0; 🔴 0 for performance
r.pathtracing=0; 🔴 0 for performance
r.raytracing.shadows.denoiser=0; 🔴 0 for performance
r.raytracing.shadows=0; 🔴 0 for performance
r.raytracing=1; 🔴 0 for performance
r.shadow.virtual.enable=1; 🔴 0 for performance
r.shadow.virtual.nonnanite.includeincoarsepages=0; 🔴 0 for performance
r.shadow.virtual.nonnanitevsm=1; 🔴 0 for performance
r.shadow.virtual.translucentquality=0; 🔴 0 for performance
;
; ue5
;
r.heterogeneousvolumes.hardwareraytracing=0;
r.lumen.hardwareraytracing.lightingmode=0;
r.lumen.radiancecache.hardwareraytracing.retrace.farfield=0;
r.lumen.radiancecache.hardwareraytracing=1;
r.lumen.reflections.hardwareraytracing.retrace.farfield=0;
r.lumen.reflections.hardwareraytracing=0;
r.lumen.screenprobegather.hardwareraytracing.retrace.farfield=0;
r.lumen.screenprobegather.hardwareraytracing=1;
r.lumen.screenprobegather.shortrangeao.hardwareraytracing=0;
r.lumen.translucencyvolume.hardwareraytracing=0;
r.lumenscene.directlighting.hardwareraytracing=1; 🔴 0 for performance
r.lumenscene.radiosity.hardwareraytracing=1; 🔴 0 for performance
r.manylights.hardwareraytracing=0;
;
; ue5
;
fx.niagara.asyncgputrace.globalsdfenabled=1;
fx.niagara.asyncgputrace.hwraytraceenabled=0;
fx.niagara.collision.cpuenabled=0;
fx.niagaraallowruntimescalabilitychanges=1;
r.distancefields.supportevenifhardwareraytracingsupported=0;
r.lumen.asynccompute=1;
r.lumen.diffuseindirect.allow=1;
r.lumen.diffuseindirect.asynccompute=1;
r.lumen.reflections.allow=1;
r.lumen.reflections.asynccompute=1;
r.lumen.reflections.distantscreentraces=1;
r.lumen.reflections.maxroughnesstotraceforfoliage=0.4;
r.lumen.reflections.screenspacereconstruction=1;
r.lumen.reflections.screentraces=1;
r.lumen.screenprobegather.materialao=1;
r.lumen.tracemeshsdfs.tracedistance=180;
r.lumen.translucencyvolume.radiancecache.probeatlasresolutioninprobes=128;
r.lumenscene.farfield=0;
r.lumenscene.lighting.asynccompute=1;
r.nanite.asyncrasterization.shadowdepths=1;
r.nanite.asyncrasterization=1;
r.nanite.streaming.asynccompute=1;
r.nanite.streaming.imposters=0;
r.nanite.viewmeshlodbias.min=-2;
r.nanite.viewmeshlodbias.offset=0;
r.raytracing.ambientocclusion=0;
r.raytracing.excludedecals=1;
r.raytracing.excludesky=1;
r.raytracing.excludetranslucent=1;
r.raytracing.geometry.cable=0;
r.raytracing.geometry.hierarchicalinstancedstaticmesh=0;
r.raytracing.geometry.instancedstaticmeshes.evaluatewpo=0;
r.raytracing.geometry.instancedstaticmeshes=0;
r.raytracing.geometry.landscape=0;
r.raytracing.geometry.landscapegrass=0;
r.raytracing.geometry.naniteproxies=1;
r.raytracing.geometry.niagarameshes=0;
r.raytracing.geometry.niagararibbons=0;
r.raytracing.geometry.niagarasprites=0;
r.raytracing.geometry.proceduralmeshes=0;
r.raytracing.geometry.skeletalmeshes=0;
r.raytracing.geometry.splinemeshes=0;
r.raytracing.geometry.staticmeshes=0;
r.raytracing.globalillumination=0;
r.raytracing.lightfunction=0;
r.raytracing.nanite.mode=0;
r.raytracing.reflections=0;
r.raytracing.shadows.acceptfirsthit=1;
r.raytracing.shadows.enablehairvoxel=0;
r.raytracing.shadows.enablematerials=0;
r.raytracing.shadows.enabletwosidedgeometry=0;
r.raytracing.shadows.lights.directional=0;
r.raytracing.shadows.lights.point=0;
r.raytracing.shadows.lights.rect=0;
r.raytracing.shadows.lights.spot=0;
r.raytracing.shadows.maxbatchsize=8;
r.raytracing.shadows.tiledprojection.downsamplemode=0;
r.raytracing.shadows.tiledprojection.filter=1;
r.raytracing.shadows.tiledprojection=1;
r.raytracing.skylight=0;
r.raytracing.translucency=0;
r.raytracing.usetexturelod=1;
r.shadow.virtual.forceonlyvirtualshadowmaps=0;
r.shadow.virtual.subsurfaceshadowmode=1;
;
; ect
;
d3d12.maximumframelatency=1;
d3d12.texturepoolonlyaccountstreamabletexture=1;
fx.gpusimulationtexturesizex=32;
fx.gpusimulationtexturesizey=32;
r.ambientocclusionmaxquality=100;
r.antialiasingmethod=0;
r.bloom.asynccompute=1;
r.bloom.screenpercentage=50;
r.blurgbuffer=0;
r.chaos.reflectioncapturestaticsceneonly=1;
r.contactshadows=1;
r.d3d.forcedxc=1;
r.d3d11.useallowtearing=1;
r.d3d12.allowasynccompute=1;
r.d3d12.allowshadermodel6=1;
r.d3d12.gpucrashdebuggingmode=0;
r.d3d12.useallowtearing=1;
r.detectandwarnofbaddrivers=0;
r.dfshadowasynccompute=1;
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
r.dynamicres.operationmode=0;
r.fidelityfx.fsr.enabled=0;
r.fidelityfx.fsr2.enabled=0;
r.fidelityfx.fsr3.enabled=0;
r.filmgrain=0;
r.filter.sizescale=1;
r.fog=1;
r.fxaa.quality=0;
r.gpucrash.collectionenable=0;
r.gpuscene.parallelupdate=1;
r.gtsynctype=0;
r.hairstrands.composeaftertranslucency=0;
r.hairstrands.deepshadow.supersampling=0;
r.hairstrands.minlod=0;
r.hairstrands.rasterizationscale=0.5;
r.hairstrands.scatterscenelighting=1;
r.hairstrands.shadow.castshadowwhennonvisible=0;
r.hairstrands.skylighting.integrationtype=2;
r.hairstrands.skylighting.screentraceocclusion=0;
r.hairstrands.velocityrasterizationscale=1;
r.hairstrands.voxelization.voxelsizeinpixel=0.3;
r.hzbocclusion=1;
r.motionblurquality=0;
r.ngx.dlss.autoexposure=1;
r.ngx.dlss.denoisermode=1;
r.ngx.dlss.dilatemotionvectors=1;
r.ngx.dlss.enable=1;
r.ngx.dlss.prefernissharpen=0;
r.ngx.dlss.quality.auto=0;
r.ngx.dlss.reflections.temporalaa=0;
r.ngx.dlss.sharpness=0;
r.ngx.dlss.waterreflections.temporalaa=0;
r.ngx.loglevel=0;
r.nis.enable=0;
r.nis.sharpness=0;
r.numbufferedocclusionqueries=2;
r.optimizedwpo=1;
r.postprocessaaquality=0;
r.postprocessing.prefercompute=1;
r.reflectioncapturesupersamplefactor=1;
r.refraction.blur.temporalaa=1;
r.scenecolorfringe.max=0;
r.scenedepthhzbasynccompute=1;
r.secondaryscreenpercentage.gameviewport=0;
r.shaders.removedeadcode=1;
r.shaders.removeunusedinterpolators=1;
r.shadow.csmshadowdistancefadeoutmultiplier=1;
r.skyatmosphere.multiscatteringlut.samplecount=15;
r.skyatmosphere.transmittancelut.samplecount=10;
r.skyatmosphereasynccompute=1;
r.ssr.experimentaldenoiser=0;
r.streaming.amortizecputogpucopy=0;
r.streaming.boost=1;
r.streaming.fullyloadusedtextures=0;
r.streaming.limitpoolsizetovram=1;
r.streaming.maxeffectivescreensize=0;
r.streaming.maxnumtexturestostreamperframe=0;
r.streaming.poolsize.vrampercentageclamp=1024;
r.streaming.poolsize=1000;
r.streaming.poolsizeformeshes=-1;
r.streaming.useallmips=0;
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=1;
r.temporalaa.quality=0;
r.temporalaasamples=8;
r.tonemapper.grainquantization=0;
r.tonemapper.quality=2;
r.tonemapper.sharpen=0;
r.volumetriccloud.distancetosamplemaxcount=15;
r.volumetriccloud.enableatmosphericlightssampling=1;
r.volumetriccloud.enabledistantskylightsampling=1;
r.volumetriccloud.shadowmap.spatialfiltering=1;
r.volumetriccloud.shadowmap=1;
r.volumetriccloud.skyao=1;
r.volumetricfog.conservativedepth=0;
r.volumetricfog.emissive=0;
r.volumetricfog.injectraytracedlights.locallights=0;
r.volumetricfog.injectraytracedlights=0;
r.volumetricfog.jitter=1;
r.volumetricfog.temporalreprojection=1;
r.volumetricrendertarget.preferasynccompute=1;
r.vrs.enable=0;
r.vrs.enableimage=0;
r.vrs.enablesoftware=0;
r.vsync=0;
r.vsyncinformationinsights=0;
r.vulkan.allowasynccompute=1;
r.water.reflections.maxroughnesstotrace=0.4;
r.water.singlelayer.depthprepass=1;
r.water.singlelayer.distancefieldshadow=0;
r.water.singlelayer.rtr=0;
r.water.singlelayer.shaderssupportdistancefieldshadow=0;
r.water.singlelayer.shaderssupportvsmfiltering=0;
r.water.singlelayer.tiledcomposite=1;
r.water.singlelayer.underwaterfogwhencameraisabovewater=0;
r.water.singlelayer.vsmfiltering=0;
r.xess.enabled=0;
rhi.maximumframelatency=1;
t.maxfps=0;
t.overridefps=0;
t.streamline.reflex.auto=1;
t.streamline.reflex.enable=1;
t.streamline.reflex.mode=2;
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
doubleclicktime=0.01; 🔴 default is 0.1
initialbuttonrepeatdelay=0.1; 🔴 default is 0.2
```

---
