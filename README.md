## updated 4/11/2026 ✂ 📋 🌀 :ramen: v1.2.9

### quality ue4/5 config and for reference/customization/optimization/learning

## open engine.ini and copy pasta %localappdata%

#### optional poolsize stuff (set to ~40% of total VRAM)
```python
r.streaming.limitpoolsizetovram=0; 0 to manually set poolsize
r.streaming.poolsize=3000; 400,600,800,1000,2000,3000,4000 to lower vram usage
r.streaming.poolsizeformeshes=-1;
```
#### optional RAM/VRAM usage/stutter, lower/raise
```python
r.rendertargetpoolmin=400; 200,400,450 to lower vram usage
r.streaming.maxtempmemoryallowed=75; 50,75,100 to lower ram usage
r.vt.poolsizescale=1; 1,2,4,8 to lower vram usage
```
#### optional DLSS/TAAU/ect scaling stuff (ultra performance, performance, balanced, quality, ultra quality)
```python
r.mipmaplodbias=-1.000; -1.585,-1.000,-0.7606,-0.5771,-0.3765
sg.resolutionquality=50; 33,50,59,67,77
```
#### optional AA stuff
```python
r.antialiasingmethod=2; ue5 0 off 1 fxaa 2 taa 3 msaa 4 tsr
r.defaultfeature.antialiasing=2; 0 off 1 fxaa 2 taa 3 msaa
r.fxaa.quality=0; 3,4 for performance
r.postprocessaaquality=6; ue4 0 off 1,2 fxaa 3,4,5,6 taa
r.temporalaa.algorithm=0; 0 for gen4 1 for gen5
r.temporalaa.historyscreenpercentage=100;
r.temporalaa.quality=2;
r.temporalaa.upsampling=1;
r.temporalaacurrentframeweight=0.04;
r.temporalaafiltersize=0.1;
r.temporalaasamples=8;
r.tsr.history.screenpercentage=100;
```
#### Your choice UE dev intent was 1 i think
```python
r.tonemapper.sharpen=1; ~0,~1,~2
```
#### optional HZBOC algorithm will crash games if set differently
```python
r.hzbocclusion=1; scene depended
```

#### check performance options (left to right, performance to quality)

#### you may need to make the Engine.ini and/or set it to read only*

#### after pasting ini start game and set graphic settings to your spec low/med/high/ultra on each setting then restart game*

```python
[core.log]
global=off;

[crashreportclient]
ballowtobecontacted=0;
bisallowedtoclosewithoutsending=1;
bsendlogfile=0;
cansendwhenuifailedtoinitialize=0;
datarouterurl=0;
uiinitretrycount=0;

[/script/engine.engine]
bpauseonlossoffocus=0;
bsmoothframerate=0;
busefixedframerate=0;

[texturestreaming]
poolsizevrampercentage=70; 50 to lower vram usage

[consolevariables]
d3d12.maximumframelatency=1;
foliage.asyncinstanebufferconversion=1;
fx.niagara.asyncgputrace.globalsdfenabled=0; 0 for performance
fx.niagara.asyncgputrace.hwraytraceenabled=0; 0 for performance
fx.niagaraallowruntimescalabilitychanges=1;
grass.disabledynamicshadows=0; 1 for performance
grass.maxupdatefrequency=10;
grass.tickinterval=1;
r.allowlandscapeshadows=1; 0 for performance
r.ambientocclusionlevels=-1; 0,1,2 for performance
r.ambientocclusionstaticfraction=-1; 0 for performance
r.anisotropicmaterials=1; 0 for performance
r.aoapplytostaticindirect=1;
r.aoglobaldistancefield.mipfactor=4; 4,8 for performance
r.aoglobaldistancefield=1;
r.aoglobaldistancefieldrepresentheightfields=1;
r.aoheightfieldocclusion=0; 0 for performance
r.aoquality=2; 0,1,2 for performance
r.aospecularocclusionmode=1;
r.blurgbuffer=0; 0,-1 for performance
r.capsuleshadows=0; 0 for performance
r.capsuleshadowsfullresolution=0;
r.chaos.reflectioncapturestaticsceneonly=1;
r.compileshadersfordevelopment=0;
r.contactshadows.nonshadowcastingintensity=0;
r.contactshadows.overrideshadowcastingintensity=-1;
r.contactshadows.standalone.method=0;
r.contactshadows=1; 0,1,2 for performance
r.d3d11.depth24bit=0; 1 for performance
r.d3d11.useallowtearing=1;
r.d3d12.allowshadermodel6=1;
r.d3d12.depth24bit=0; 1 for performance
r.d3d12.gpucrashdebuggingmode=0;
r.d3d12.shadowdepth32bit=0; 0 for performance
r.d3d12.useallowtearing=1;
r.depthoffieldquality=1; 0,1 for performance
r.detectandwarnofbaddrivers=0;
r.dffullresolution=0; 0 for performance
r.dfshadowquality=2; 0,1,2,3 for performance
r.distancefieldao=1; 0 for performance
r.distancefieldshadowing=1; 0 for performance
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
r.dof.temporalaaquality=1; 0 for performance
r.dynamicres.operationmode=0;
r.filmgrain=0;
r.filter.loopmode=0;
r.filter.sizescale=1;
r.finishcurrentframe=0; 1 for latency cost too much
r.fog=1;
r.forwardshading.forceskylightcubemapblending=0; 0 for performance
r.gpucrash.collectionenable=0;
r.hairstrands.composeaftertranslucency=1;
r.hairstrands.deepshadow.supersampling=0;
r.hairstrands.interpolation.usesingleguide=1; 1 for performance
r.hairstrands.minlod=0;
r.hairstrands.rasterizationscale=0.5;
r.hairstrands.scatterscenelighting=0; 0,1 for performance
r.hairstrands.shadow.castshadowwhennonvisible=1; 0 for performance
r.hairstrands.skyao=0; 0 for performance
r.hairstrands.skylighting.integrationtype=2;
r.hairstrands.skylighting.jitterintegration=0;
r.hairstrands.skylighting.screentraceocclusion=0;
r.hairstrands.usecardsinsteadofstrands=0; 1 for performance
r.hairstrands.velocityrasterizationscale=0.5; 0.5,1 for performance
r.hairstrands.visibility.msaa.sampleperpixel=1; 1,2 for performance
r.hairstrands.visibility.ppll=0;
r.heightfieldshadowing=0;
r.instanceculling.occlusioncull=1; scene depended
r.landscapelodbias=0; 1 for performance
r.lightmaxdrawdistancescale=1; 0.6,0.85,1 for performance
r.lumen.diffuseindirect.allow=1;
r.lumen.diffuseindirect.ssao=0; 0 for performance
r.lumen.hardwareraytracing.hitlighting.reflectioncaptures=1; 1 for performance
r.lumen.hardwareraytracing.lightingmode=0; 0 for performance
r.lumen.hardwareraytracing=1; 0 for performance
r.lumen.reflections.allow=1;
r.lumen.reflections.asynccompute=0;
r.lumen.reflections.bilateralfilter=0; 0 for performance
r.lumen.reflections.distantscreentraces=1;
r.lumen.reflections.downsamplefactor=1; 2 for performance
r.lumen.reflections.hairstrands.screentrace=0;
r.lumen.reflections.hairstrands.voxeltrace=0;
r.lumen.reflections.hardwareraytracing=1; 0 for performance
r.lumen.reflections.hierarchicalscreentraces.maxiterations=50;
r.lumen.reflections.hierarchicalscreentraces.minimumoccupancy=0;
r.lumen.reflections.maxbounces=1; 1,2 for performance
r.lumen.reflections.maxroughnesstotrace=0.4; -1,0.4 for performance
r.lumen.reflections.maxroughnesstotraceforfoliage=0.4;
r.lumen.reflections.roughnessfadelength=0.1;
r.lumen.reflections.samplescenecolorathit=1;
r.lumen.reflections.screenspacereconstruction.tonemapstrength=0;
r.lumen.reflections.screenspacereconstruction=1;
r.lumen.reflections.screentraces=1;
r.lumen.reflections.smoothbias=0.4; 0,0.4 for performance
r.lumen.reflections.specularindirectbuffer32bit=1; 1 for performance
r.lumen.reflections.temporal=1;
r.lumen.reflections.tracemeshsdfs=0; 0 for performance
r.lumen.screenprobegather.downsamplefactor=32; 32,16 for performance
r.lumen.screenprobegather.fullresolutionjitterwidth=1;
r.lumen.screenprobegather.irradianceformat=1; 1,0 for performance
r.lumen.screenprobegather.materialao=1;
r.lumen.screenprobegather.radiancecache.proberesolution=32; 16,32 for performance
r.lumen.screenprobegather.screenspacebentnormal=1;
r.lumen.screenprobegather.screentraces.hzbtraversal.fullresdepth=0; 0,1 for performance
r.lumen.screenprobegather.shortrangeao.hairscreentrace=1; 0,1 for performance
r.lumen.screenprobegather.shortrangeao.hairvoxeltrace=0; 0 for performance
r.lumen.screenprobegather.shortrangeao=1; 0 for performance
r.lumen.screenprobegather.stochasticinterpolation=1; 1,0 for performance
r.lumen.screenprobegather.tracingoctahedronresolution=16; 8,16 for performance
r.lumen.screenprobegather.twosidedfoliagebackfacediffuse=0; 0,1 for performance
r.lumen.tracemeshsdfs.allow=1; 0 for performance
r.lumen.tracemeshsdfs=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.allow=1; 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enableforproject=0; 0 for performance
r.lumen.translucencyvolume.enable=1; 0 for performance
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0; 0 for performance
r.lumenscene.farfield=0;
r.lumenscene.radiosity.hemisphereproberesolution=3; 2,3 for performance
r.lumenscene.radiosity.probespacing=8; 16,8,4 for performance
r.maxanisotropy=16; 0,4,8 for performance
r.meshstreaming=1;
r.minscreenradiusfordepthprepass=0.03; 0.03,0 for performance
r.minscreenradiusforlights=0.03; 0.06,0.04 for performance
r.motionblurquality=0;
r.nanite.allowtessellation=0;
r.nanite.computerasterization=1;
r.nanite.disablefallbackmeshes=0;
r.nanite.softwarevrs=1;
r.nanite.usepregeneratedinstancesbuffer=1;
r.ngx.dlss.prefernissharpen=0;
r.ngx.dlss.quality.auto=0;
r.ngx.dlss.reflections.temporalaa=1;
r.ngx.dlss.sharpness=0.5;
r.ngx.dlss.waterreflections.temporalaa=1;
r.ngx.loglevel=0;
r.nis.enable=0;
r.nis.sharpness=0;
r.numbufferedocclusionqueries=1;
r.oneframethreadlag=1; 0 for latency cost too much
r.optimizedwpo=1;
r.pathtracing=0;
r.postprocessing.prefercompute=0; gpu depended
r.postprocessing.quarterresolutiondownsample=0; 1 for performance
r.raytracing.ambientocclusion=0;
r.raytracing.enable=0; 0 disables lumen hardwareraytracing
r.raytracing.enableingame=0; 0 disables lumen hardwareraytracing
r.raytracing.forceallraytracingeffects=0;
r.raytracing.globalillumination=0;
r.raytracing.lightfunction=0;
r.raytracing.reflections=0;
r.raytracing.shadows=0;
r.raytracing.skylight=0;
r.raytracing.translucency=0;
r.raytracing=0; 0 disables lumen hardwareraytracing
r.reflectioncapturesupersamplefactor=1; 1 for performance
r.refraction.blur.temporalaa=1;
r.refraction.blur=0;
r.refraction.offsetquality=1;
r.scenecolorformat=3; 2,3,4 for performance
r.scenecolorfringe.max=0;
r.sceneculling.explicitcellbounds=0; 0 for performance
r.screenpercentage.default=100;
r.screenpercentage.maxresolution=0;
r.screenpercentage.minresolution=0;
r.screenpercentage=100;
r.secondaryscreenpercentage.gameviewport=0;
r.shaders.removedeadcode=1;
r.shaders.removeunusedinterpolators=1;
r.shadow.csm.transitionscale=1;
r.shadow.csmshadowdistancefadeoutmultiplier=1;
r.shadow.forcesinglesampleshadowingfromstationary=0;
r.shadow.nanitelodbias=0;
r.shadow.preshadowresolutionfactor=0.5; 0.5,1 for performance
r.shadow.radiusthreshold=0.04; 0.06,0.05,0.04 for performance
r.shadow.virtual.enable=1; 0 for performance
r.shadow.virtual.forceonlyvirtualshadowmaps=1;
r.shadow.virtual.nonnanite.includeincoarsepages=0; 0,1 for performance
r.shadow.virtual.onepassprojection.maxlightsperpixel=8; 4,8,16,32 for performance
r.shadow.virtual.onepassprojection=1; 1 for performance
r.shadow.virtual.resolutionlodbiasdirectional=1; 1,0.5,0 for performance
r.shadow.virtual.resolutionlodbiasdirectionalmoving=1; 1,0.5,0 for performance
r.shadow.virtual.resolutionlodbiaslocal=1; 1,0.5,0 for performance
r.shadow.virtual.resolutionlodbiaslocalmoving=1; 1,0.5,0 for performance
r.shadow.virtual.smrt.adaptiveraycount=1;
r.shadow.virtual.smrt.raycountdirectional=4; 4,8 for performance
r.shadow.virtual.smrt.raycountlocal=4; 4,8 for performance
r.shadow.virtual.smrt.raylengthscaledirectional=1.5;
r.shadow.virtual.smrt.reduceraysatdistance=1; 1 for performance
r.shadow.virtual.smrt.samplesperraydirectional=1;
r.shadow.virtual.smrt.samplesperrayhair=1;
r.shadow.virtual.smrt.samplesperraylocal=1;
r.shadow.virtual.smrt.texelditherscaledirectional=2;
r.shadow.virtual.smrt.texelditherscalelocal=2;
r.shadow.virtual.translucentquality=0; 0 for performance
r.shadowquality=4; 3,4,5 for performance
r.skyatmosphere.fastskylut.samplecountmax=32; 32,64 for performance
r.skyatmosphere.fastskylut.samplecountmin=1; 1,4 for performance
r.skyatmosphere.lut32=0; 0 for performance
r.skyatmosphere.multiscatteringlut.highquality=0; 0 for performance
r.skyatmosphere.multiscatteringlut.samplecount=15;
r.skyatmosphere.samplecountmax=32; 32,64 for performance
r.skyatmosphere.samplecountmin=1; 1,4 for performance
r.skyatmosphere.samplelightshadowmap=0; 0 for performance
r.skyatmosphere.transmittancelut.samplecount=10;
r.skyatmosphere.transmittancelut.usesmallformat=0; 1 for performance
r.ssgi.enable=0; 0 for performance
r.ssgi.quality=2; 2,3 for performance
r.ssr.halfresscenecolor=1; 1 for performance
r.ssr.quality=2; 0,2 for performance
r.sss.burley.quality=0; 0,1 for performance
r.sss.checkerboard=1; 1,2 for performance
r.sss.halfres=0; 1 for performance
r.sss.quality=1; 0 for performance
r.streaming.amortizecputogpucopy=0;
r.streaming.boost=1;
r.streaming.dropmips=0; 1 to lower vram usage
r.streaming.fullyloadmeshes=0;
r.streaming.fullyloadusedtextures=0;
r.streaming.hiddenprimitivescale=0.5; 0,0.25,0.5 for performance
r.streaming.maxeffectivescreensize=0;
r.streaming.maxnumtexturestostreamperframe=0;
r.streaming.mipbias=0; 1 for performance
r.streaming.poolsize.vrampercentageclamp=1024;
r.streaming.useallmips=0;
r.streaming.useasyncrequestsforddc=1;
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=0; 0,1 for performance
r.subsurfacescattering=1; 0 for performance
r.supportmateriallayers=1; 0 for performance
r.tessellationadaptivepixelspertriangle=999999; 999999,48 for performance
r.translucencylightingvolumedim=48; 32,48,64 for performance
r.translucencyvolumeblur=1; 0 for performance
r.volumetriccloud.distancetosamplemaxcount=15;
r.volumetriccloud.enableatmosphericlightssampling=1;
r.volumetriccloud.enabledistantskylightsampling=1;
r.volumetriccloud.enablelocallightssampling=0; 0 for performance
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 0 for performance
r.volumetriccloud.shadowmap.spatialfiltering=0; 0 for performance
r.volumetriccloud.shadowmap=0; 0 for performance
r.volumetriccloud.skyao=0;
r.volumetriccloud=1; 0 for performance
r.volumetricfog.conservativedepth=0;
r.volumetricfog.emissive=0; 0 for performance
r.volumetricfog.historymisssupersamplecount=2; 2 for performance
r.volumetricfog.injectraytracedlights.locallights=0; 0 for performance
r.volumetricfog.injectshadowedlights=0; 0 for performance
r.volumetricfog.injectshadowedlightsseparately=0; 0,1 for performance
r.volumetricfog.lightfunction=0;
r.volumetricfog.temporalreprojection=1;
r.volumetricfog.upsamplejittermultiplier=0; 0 for performance
r.volumetricfog.useslightfunctionatlas=1;
r.volumetricfog=1; 0 for performance
r.vrs.contrastadaptiveshading=0;
r.vrs.decals=0;
r.vrs.enable=0;
r.vrs.enableimage=0;
r.vrs.enablesoftware=1;
r.vsync=0;
r.vt.anisotropicfiltering=1; 0 for performance
r.vt.maxanisotropy=4; 2,4,8 for performance
r.water.enableshallowwatersimulation=0; 0 for performance
r.water.enableunderwaterpostprocess=0; 0 for performance
r.water.reflections.maxroughnesstotrace=0.4; 0.4,0.6 for performance
r.water.singlelayer.distancefieldshadow=1; 0 for performance
r.water.singlelayer.reflection=1; 0,3,1 for performance
r.water.singlelayer.refractiondownsamplefactor=1; 1,2 for performance
r.water.singlelayer.rtr=0;
r.water.singlelayer.shaderssupportdistancefieldshadow=1; 0 for performance
r.water.singlelayer.shaderssupportvsmfiltering=0; 0,1 for performance
r.water.singlelayer.ssr=1; 0 for performance
r.water.singlelayer.tiledcomposite=1;
r.water.singlelayer.underwaterfogwhencameraisabovewater=0;
r.water.singlelayer.vsmfiltering=0; 0,1 for performance
r.water.watermesh.tessfactorbias=0; -1 for performance
rhi.maximumframelatency=1;
```

---

## open input.ini and copy pasta %localappdata%

```python
[/script/engine.inputsettings]
baltentertogglesfullscreen=1;
benablemousesmoothing=0;
bf11togglesfullscreen=0;
buttonrepeatdelay=0.1;
bviewaccelerationenabled=0;
doubleclicktime=0.01; default is 0.1
initialbuttonrepeatdelay=0.1; default is 0.2
```

---

## ect

```python
## upscaling to use
2560x1440 use 58%,67%,70% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3328x1872 use 50%,58%,67% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3840x2160 use 33%,50%,58%,67% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

## repak.bat method
zzz_inimods\engine\config\windows\windowsengine.ini
zzz_inimods\engine\config\windows\windowsinput.ini
```

---
