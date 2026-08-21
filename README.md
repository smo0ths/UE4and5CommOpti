## updated 8/21/2026 ✂ 📋 🌀 :ramen: v1.4.0

### quality ue4/5 config and for reference/customization/optimization/learning

## open Engine.ini and copy pasta %localappdata%

#### check performance options (left to right, performance to quality)

#### you may need to make the Engine.ini and/or set it to read only*

#### after pasting ini start game and set graphic settings to your spec low/med/high/ultra on each setting then restart game*

#### you may need to delete *game*_PCD3D_SM6.upipelinecache and restart game a few times if it crashes because of runtime stuff

#### add optional under config, optional cvars with test* next to them you may want to skip

---

#### poolsize/ram/vram
```python
r.rendertargetpoolmin=450; 200,400,450 to lower vram usage
r.streaming.limitpoolsizetovram=0; 0 to manually set poolsize
r.streaming.maxtempmemoryallowed=100; 50,75,100 to lower ram usage
r.streaming.poolsize=4000; 400,600,800,1000,2000,3000,4000 to lower vram usage
r.streaming.poolsizeformeshes=-1;
r.vt.poolsizescale=1; 1,2,4,8 to lower vram usage
```
#### optional scaling (ultra performance, performance, balanced, quality, ultra quality, native/dlaa)
```python
r.mipmaplodbias=-1.000; -1.585,-1.000,-0.7606,-0.5771,-0.3765,0
sg.resolutionquality=50; 33,50,59,67,77,100
```
#### AA/scaling
```python
r.antialiasingmethod=2; ue5 0 off 1 fxaa 2 taa 3 msaa 4 tsr
r.defaultfeature.antialiasing=2; 0 off 1 fxaa 2 taa 3 msaa
r.dynamicres.operationmode=0;
r.fxaa.quality=0; 3,4 for performance
r.ngx.dlss.prefernissharpen=0;
r.ngx.dlss.quality.auto=0;
r.ngx.dlss.reflections.temporalaa=1;
r.ngx.dlss.sharpness=0.5;
r.ngx.dlss.waterreflections.temporalaa=1;
r.ngx.loglevel=0;
r.nis.enable=0;
r.nis.sharpness=0;
r.postprocessaaquality=6; ue4 0 off 1,2 fxaa 3,4,5,6 taa
r.screenpercentage.default=100;
r.screenpercentage.maxresolution=0;
r.screenpercentage.minresolution=0;
r.screenpercentage=100;
r.secondaryscreenpercentage.gameviewport=0;
r.temporalaa.algorithm=0; 0 for gen4 1 for gen5
r.temporalaa.historyscreenpercentage=100;
r.temporalaa.quality=1; 1,2 for performance
r.temporalaa.upsampling=1;
r.temporalaacurrentframeweight=0.04;
r.temporalaafiltersize=0.1;
r.temporalaasamples=8;
r.tsr.history.screenpercentage=100;
```
#### quality 1
```python
fx.niagara.collision.cpuenabled=0; gpu dependent test
fx.niagara.qualitylevel=2; 0,1,2,3 for performance
grass.disabledynamicshadows=0; 1 for performance
r.allowlandscapeshadows=1; 0 for performance
r.ambientocclusionlevels=-1; 0,1,2 for performance
r.ambientocclusionmaxquality=-60;
r.ambientocclusionstaticfraction=-1; 0 for performance
r.anisotropicmaterials=1; 0 for performance
r.aoquality=1; 0,1,2 for performance
r.capsuleshadows=1; 0,1 for performance
r.contactshadows=1; 0,1 for performance
r.detailmode=1; 0,1,2,3 for performance
r.dfshadowquality=2; 0,1,2,3 for performance
r.distancefieldao=1; 0 for performance
r.distancefieldshadowing=1; 0 for performance
r.emitterspawnratescale=1; 0.125,0.25,0.5,1 for performance
r.fog=1;
r.forwardshading.forceskylightcubemapblending=0; 0 for performance test
r.landscapelodbias=0; 1 for performance
r.lightfunctionquality=1; 1,2 for performance
r.lightmaxdrawdistancescale=1; 0.6,0.85,1 for performance
r.lumen.reflections.maxbounces=1; 0,1,2 to 8 to 64 for performance test
r.lumen.reflections.maxroughnesstotrace=0.4; -1,0.4 for performance
r.lumen.reflections.maxroughnesstotraceclamp=0.4; def 1
r.lumen.reflections.maxroughnesstotraceforfoliage=0.4;
r.lumen.reflections.samplescenecolorathit=1; 0,1,2 for performance test
r.lumen.reflections.smoothbias=0.4; 0,0.4 for performance
r.lumen.reflections.tracemeshsdfs=0; 0 for performance
r.materialqualitylevel=1; 0,2,1 for performance
r.maxanisotropy=16; 0,4,8 for performance
r.minscreenradiusforlights=0.015; 0.06,0.04,0.03,0.015 for performance test
r.particlelightquality=2; 0,1,2 for performance
r.refractionquality=1; 0,1,2 for performance
r.scenecolorformat=4; 2,3,4 for performance
r.shadowquality=5; 3,4,5 for performance
r.ssgi.quality=0; 0,2,3 for performance
r.ssr.quality=2; 0,2,3 for performance
r.sss.burley.bilateralfilterkernelfunctiontype=1; 0,1 for performance
r.sss.burley.quality=1; 0,1 for performance
r.sss.checkerboard=2; 1,2,0 for performance
r.sss.quality=1; 0,-1,1 for performance
r.subsurfacescattering=1; 0 for performance
r.supportmateriallayers=1; 0 for performance
r.volumetriccloud=1; 0 for performance
r.volumetricfog=1; 0 for performance
r.vt.anisotropicfiltering=1; 0 for performance
r.vt.maxanisotropy=4; 2,4,8 for performance
r.water.enableshallowwatersimulation=0; 0 for performance test
r.water.enableunderwaterpostprocess=1; 0,1 for performance test
r.water.reflections.maxroughnesstotrace=0.4; 0.4,0.6 for performance
r.water.singlelayer.reflection=1; 0,3,1 for performance
r.water.singlelayer.ssr=1; 0 for performance
```
#### quality 2
```python
r.bloom.screenpercentage=50;
r.bloomquality=4;
r.blurgbuffer=0; 0,-1 for performance
r.depthoffieldquality=1; 0,1 for performance
r.dof.gather.accumulatorquality=0;
r.dof.gather.enablebokehsettings=0;
r.dof.gather.postfiltermethod=1;
r.dof.gather.resolutiondivisor=2;
r.dof.gather.ringcount=3;
r.dof.kernel.maxbackgroundradius=0.012;
r.dof.kernel.maxforegroundradius=0.012;
r.dof.recombine.quality=0;
r.dof.scatter.backgroundcompositing=0;
r.dof.scatter.enablebokehsettings=0;
r.dof.scatter.foregroundcompositing=0;
r.dof.scatter.maxspriteratio=0.04;
r.dof.temporalaaquality=1; 0 for performance
r.filmgrain=0;
r.filter.loopmode=0;
r.filter.sizescale=1;
r.lensflarequality=2; 0,1,2
r.lightshaftquality=1; 0,1
r.motionblur.halfresgather=1;
r.motionblur.halfresinput=1;
r.motionblurquality=0;
r.postprocessing.quarterresolutiondownsample=0; 1 for performance
r.reflectioncapturesupersamplefactor=1; 1 for performance
r.refraction.blur.temporalaa=1;
r.refraction.blur=1;
r.refraction.offsetquality=1;
r.scenecolorfringe.max=0;
r.scenecolorfringequality=0; 0,1
r.tonemapper.quality=5; 0,2,5
r.tonemapper.sharpen=1; 0,1,2
r.upscale.quality=3; 1,2,3
```
#### optional quality 3 test
```python
r.dynamicglobalilluminationmethod=1; 0 none 1 lumen 2 ssgi test
r.heterogeneousvolumes=1; 0,1 test
r.lumenscene.farfield=1; 0,1 test
r.megalights.allowed=0; test
r.nanite.allowtessellation=0; 0,1 for performance
r.nanite.tessellation=0; 0,1 for performance
r.reflectionmethod=1; 0 none 1 lumen 2 ssr test
r.tileddeferredshading.minimumcount=80; test
r.tileddeferredshading=0; test
r.useclustereddeferredshading=0; test
```
#### optional lumen quality switches
```python
r.lumen.diffuseindirect.allow=1; test
r.lumen.reflections.allow=1;
r.lumen.tracemeshsdfs.allow=0; 0,1 for performance
r.lumen.translucencyreflections.frontlayer.allow=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enableforproject=0; 0 for performance
```
#### optional HDR test
```python
r.allowhdr=0;
r.hdr.enablehdroutput=0;
```
#### optional foliage test
```python
foliage.minimumscreensize=0.000015; 0.000025,0.000015,0.000005 for performance test
foliage.minlod=-1; test
```
#### optional raytracing/hardware raytracing/lumen software raytracing test
```python
r.lumen.hardwareraytracing.hitlighting.reflectioncaptures=0; 0 for performance
r.lumen.hardwareraytracing.lightingmode=0; 0 for performance
r.lumen.hardwareraytracing=1; 0 for performance
r.lumen.reflections.hardwareraytracing.translucent.refraction.enableforproject=0; test
r.lumen.reflections.hardwareraytracing=1; 0 for performance
r.lumen.screenprobegather.shortrangeao.hardwareraytracing=0; 0 for performance
r.lumenscene.directlighting.hardwareraytracing.forcetwosided=0;
r.megalights.hardwareraytracing.farfield=0; test
r.pathtracing=0;
r.raytracing.ambientocclusion=0;
r.raytracing.enable=0; 0 disables lumen hardwareraytracing
r.raytracing.enableingame=0; 0 disables lumen hardwareraytracing
r.raytracing.enableondemand=0;
r.raytracing.forceallraytracingeffects=0;
r.raytracing.globalillumination=0;
r.raytracing.lightfunction=0;
r.raytracing.reflections=0;
r.raytracing.scene.buildmode=0; test
r.raytracing.shadows=0;
r.raytracing.skylight=0;
r.raytracing.translucency=0;
r.raytracing=0; 0 disables lumen hardwareraytracing
```
#### optional experimental test
```python
d3d12.adjusttexturepoolsizebasedonbudget=0; 1 is experimental test
r.nanite.streaming.reservedresources=1; 1 is experimental test
```
#### optional per instance occlusion culling for GPU instance culling test
```python
r.instanceculling.occlusioncull=1; scene depended test
```
#### optional HZBOC algorithm will crash games if set differently test
```python
r.hzbocclusion=1; scene depended test
```
#### optional Number of frames to buffer occlusion queries test 2
```python
r.numbufferedocclusionqueries=1; test
```
#### optional compute test
```python
r.nanite.computerasterization=1;
r.postprocessing.prefercompute=0; gpu dependent
```
#### optional parallelupdate test
```python
r.distancefields.parallelupdate=1; def 0 test
r.gpuscene.parallelupdate=1; def 0 test
r.lumenscene.parallelupdate=1; def 1
```
#### optional async test
```python
grass.grassmap.useasyncfetch=1; def 0 test
r.dfshadowasynccompute=1; def 0 test
r.enableasynccomputetranslucencylightingvolumeclear=1; def 0 test
r.lumen.reflections.asynccompute=1; def 0 test
r.megalights.asynccompute.generatesamples=1; def 0 test
r.megalights.asynccompute.volume=1; def 0 test
r.nanite.asyncrasterization.shadowdepths=1; def 0 test
r.postprocessing.forceasyncdispatch=1; def 0 test
r.raytracing.asyncbuild=1; def 0 test
r.scenedepthhzbasynccompute=1; def 0 test
r.shadow.shadowmapsrenderearly=1; def 0 test
r.skyatmosphereasynccompute=1; def 0 test
r.volumetricrendertarget.preferasynccompute=1; def 0 test
```
#### optional async defaults test
```python
allowasyncrenderthreadupdates=1; def 1
allowasyncrenderthreadupdatesduringgamethreadupdates=1; def 1 test
fx.niagara.allowasyncworktoendofframe=1; def 1 test
fx.niagara.allowdeferredreset=1; def 1 test
fx.niagara.allowvisibilitycullingfordynamicbounds=1; def 1 test
fx.niagara.asyncgputrace.globalsdfenabled=1; def 1 test
fx.niagara.asyncgputrace.hwraytraceenabled=1; def 1 test
fx.niagara.compilevalidatemode=1; def 1 test
fx.niagara.datachannels.allowasyncload=1; def 1 test
fx.niagara.datachannels.blockasyncloadonuse=1; def 1 test
fx.niagara.delayscriptasyncoptimization=1; def 1 test
fx.niagara.solo.allowasyncworktoendofframe=1; def 1 test
fx.niagara.systemsimulation.allowasync=1; def 1 test
p.useasyncinterpolation=1; def 1 test
r.ambientocclusion.asynccomputebudget=1; def 1 test
r.aoasyncbuildqueue=1; def 1 test
r.asynccachematerialuniformexpressions=1; def 1 test
r.asynccachemeshdrawcommands=1; def 1 test
r.asynccreatelightprimitiveinteractions=1; def 1 test
r.asyncpipelinecompile=1; def 1 test
r.bloom.asynccompute=1; def 1 test
r.d3d12.allowasynccompute=1; def 1 test
r.d3d12.allowpayloadmerge=1; def 1 test
r.exrreadergpu.useuploadheap=1; def 1 test
r.landscapeuseasynctasksforlodcomputation=1; def 1 test
r.localfogvolume.tilecullinguseasync=1; def 1 test
r.lumen.asynccompute=1; def 1 test
r.lumen.diffuseindirect.asynccompute=1; def 1 test
r.lumenscene.lighting.asynccompute=1; def 1 test
r.meshcardrepresentation.async=1; def 1 test
r.nanite.asyncrasterization=1; def 1 test
r.nanite.materialbuffers.asyncupdates=1; def 1 test
r.nanite.streaming.async=1; def 1 test
r.nanite.streaming.asynccompute=1; def 1 test
r.rdg.asynccompute=1; def 1 test
r.rdg.paralleldestructions=1; def 1 test
r.rdg.parallelsetup=1; def 1 test
r.sceneculling.async.query=1; def 1 test
r.sceneculling.async.update=1; def 1 test
r.stencillodmode=2; def 2 test
r.streaming.useasyncrequestsforddc=1; def 1 test
r.substrate.asyncclassification=1; def 1 test
r.tsr.asynccompute=2; def 2 test
r.uniformexpressioncacheasyncupdates=1; def 1 test
r.vt.asyncpagerequesttask=1; def 1 test
```

---

## base config:

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

[gametelemetry]
queryurl=;
ingesturl=;
configurl=;
sendinterval=;
maxbuffersize=;
querytakelimit=;
authenticationkey=;
configkey=;
maxuniquemessages=;
maxcountpermessage=;
logwarnings=;

[/script/engine.engine]
bpauseonlossoffocus=0;
bsmoothframerate=0;
busefixedframerate=0;

[texturestreaming]
poolsizevrampercentage=70; 50 to lower vram usage

[consolevariables]
d3d12.maximumframelatency=1;
foliage.minocclusionqueriespercomponent=2; 6,2 test
foliage.shadowlodbias=1; test
fx.niagaraallowruntimescalabilitychanges=1;
grass.maxupdatefrequency=10;
grass.tickinterval=1;
r.allowsubprimitivequeries=0 ; 0,1 test
r.ambientocclusion.method=0;
r.ambientocclusionmiplevelfactor=0.6;
r.ambientocclusionradiusscale=1;
r.aoapplytostaticindirect=1;
r.aoglobaldistancefield.mipfactor=4; 8,4 for performance
r.aoglobaldistancefield=1;
r.aoglobaldistancefieldrepresentheightfields=1;
r.aohistorydistancethreshold=60 ; 60,30 test
r.aohistoryweight=0.95 ; 0.85,0.95 test
r.aospecularocclusionmode=0; 0,1 test
r.capsuleshadowsfullresolution=0;
r.chaos.reflectioncapturestaticsceneonly=1;
r.compileshadersfordevelopment=0;
r.contactshadows.nonshadowcastingintensity=0;
r.contactshadows.overrideshadowcastingintensity=-1;
r.contactshadows.standalone.method=0;
r.d3d11.depth24bit=0; 1 for performance
r.d3d11.useallowtearing=1;
r.d3d12.allowshadermodel6=1;
r.d3d12.depth24bit=0; 1 for performance
r.d3d12.gpucrashdebuggingmode=0;
r.d3d12.shadowdepth32bit=0; 0 for performance
r.d3d12.useallowtearing=1;
r.detectandwarnofbaddrivers=0;
r.dffullresolution=0; 0 for performance
r.emitter.fastpoolenable=1;
r.emitter.fastpoolmaxfreesize=4194304; 2097152,4194304 test
r.finishcurrentframe=0; 1 for latency cost too much
r.gbufferdiffusesampleocclusion=0; 0,1 for performance
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
r.lumen.diffuseindirect.ssao=0; test
r.lumen.heightfog=0; test
r.lumen.reflections.bilateralfilter=0; 0 for performance
r.lumen.reflections.distantscreentraces=1;
r.lumen.reflections.downsamplefactor=1; 2 for performance
r.lumen.reflections.hairstrands.screentrace=0;
r.lumen.reflections.hairstrands.voxeltrace=0;
r.lumen.reflections.hierarchicalscreentraces.maxiterations=50;
r.lumen.reflections.hierarchicalscreentraces.minimumoccupancy=0;
r.lumen.reflections.roughnessfadelength=0.1;
r.lumen.reflections.screenspacereconstruction.tonemapstrength=0; test
r.lumen.reflections.screenspacereconstruction=1;
r.lumen.reflections.screentraces=1;
r.lumen.reflections.temporal=1;
r.lumen.screenprobegather.downsamplefactor=32; 32,16 for performance
r.lumen.screenprobegather.fullresolutionjitterwidth=1;
r.lumen.screenprobegather.integratedownsamplefactor=2; 2,1 for performance
r.lumen.screenprobegather.irradianceformat=0; test
r.lumen.screenprobegather.materialao=1; test
r.lumen.screenprobegather.radiancecache.proberesolution=32; 16,32 for performance
r.lumen.screenprobegather.screenspacebentnormal=1; test
r.lumen.screenprobegather.screentraces.hzbtraversal.fullresdepth=0; 0,1 for performance
r.lumen.screenprobegather.screentraces=1; test
r.lumen.screenprobegather.shortrangeao.bentnormal=0; test
r.lumen.screenprobegather.shortrangeao.hairscreentrace=0; test
r.lumen.screenprobegather.shortrangeao.hairvoxeltrace=0; 0 for performance
r.lumen.screenprobegather.shortrangeao=1; test
r.lumen.screenprobegather.stochasticinterpolation=1; 1,0 for performance
r.lumen.screenprobegather.temporal.distancethreshold=0.015; 0.015,0.005 test
r.lumen.screenprobegather.tracingoctahedronresolution=10; 8,10,16 for performance test
r.lumen.screenprobegather.twosidedfoliagebackfacediffuse=0; 0,1 for performance
r.lumen.tracemeshsdfs=0; 0 for performance
r.lumen.translucencyvolume.enable=1; test
r.lumen.translucencyvolume.gridpixelsize=64; 64,32 for performance
r.lumen.translucencyvolume.radiancecache=0; test
r.lumen.translucencyvolume.tracefromvolume=0; test
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0; 0 for performance test
r.lumenscene.radiosity.hemisphereproberesolution=3; 2,3 for performance
r.lumenscene.radiosity.probespacing=8; 16,8,4 for performance
r.materiallogerroronfailure=0;
r.nanite.allowskinnedmeshes=1; 0,1 test
r.nanite.decompressdepth=0; 1 for performance test
r.nanite.dicingrate=4; test
r.nanite.disablefallbackmeshes=0;
r.nanite.maxpixelsperedge=1; 4,3,2,1 for performance
r.nanite.shadowraster.minpixelradius=16; 32,24,16,8,0 for performance test
r.nanite.softwarevrs=1;
r.nanite.usepregeneratedinstancesbuffer=1;
r.oneframethreadlag=1; 0 for latency cost too much
r.raytracing.excludedecals=1; def 0 test
r.raytracing.excludesky=1; def 1
r.raytracing.excludetranslucent=0; def 0
r.sceneculling.explicitcellbounds=0; 0 for performance
r.shaders.removedeadcode=1;
r.shaders.removeunusedinterpolators=1;
r.shadow.buildinglightcomponentshadows=0; 0,1 for performance
r.shadow.csm.transitionscale=1;
r.shadow.csmshadowdistancefadeoutmultiplier=1;
r.shadow.cullminorshadowcasters=0; 0,1 for performance
r.shadow.detectvertexshaderlayeratruntime=1; test
r.shadow.forcesinglesampleshadowingfromstationary=0;
r.shadow.itemlightcomponentshadows=1; 0,1 for performance
r.shadow.nanitelodbias=1; 2,1,0 for performance test
r.shadow.preshadowresolutionfactor=0.5; 0.5,1 for performance
r.shadow.radiusthreshold=0.04; 0.06,0.05,0.04 for performance
r.shadow.virtual.cache.forceinvalidatedirectional=1; 1,0 test
r.shadow.virtual.cache.maxmaterialpositioninvalidationrange=2500; test
r.shadow.virtual.enable=1; 0 for performance
r.shadow.virtual.forceonlyvirtualshadowmaps=1;
r.shadow.virtual.markpixelpagesmipmodelocal=0; 1,0 for performance
r.shadow.virtual.maxphysicalpages=2048; 512,1024,2048,4096 test
r.shadow.virtual.nonnanite.includeincoarsepages=0; 0,1 for performance
r.shadow.virtual.onepassprojection.maxlightsperpixel=8; 4,8,16,32 for performance
r.shadow.virtual.onepassprojection=1; 1 for performance
r.shadow.virtual.resolutionlodbiasdirectional=-0.5; 0,-0.5,-1.5 test
r.shadow.virtual.resolutionlodbiasdirectionalmoving=-0.5; 0,-0.5,-1.5 test
r.shadow.virtual.resolutionlodbiaslocal=0; 1,0 test
r.shadow.virtual.resolutionlodbiaslocalmoving=1; 2,1 test
r.shadow.virtual.smrt.adaptiveraycount=1;
r.shadow.virtual.smrt.raycountdirectional=4; 0,4,8 test
r.shadow.virtual.smrt.raycountlocal=4; 0,4,8 test
r.shadow.virtual.smrt.raylengthscaledirectional=1.5; test
r.shadow.virtual.smrt.reduceraysatdistance=1; 1 for performance
r.shadow.virtual.smrt.samplesperraydirectional=2; 1,2,4 test
r.shadow.virtual.smrt.samplesperrayhair=1;
r.shadow.virtual.smrt.samplesperraylocal=2; 1,2,4 test
r.shadow.virtual.smrt.texelditherscaledirectional=2;
r.shadow.virtual.smrt.texelditherscalelocal=2;
r.shadow.virtual.translucentquality=0; 0 for performance
r.shadow.virtual.usehzb=1; 1,2 for performance
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
r.ssr.halfresscenecolor=1; 1,0 for performance
r.ssr.temporal=1;
r.ssr.tiledcomposite=0; test
r.sss.halfres.forceseparable=1; 1,0 for performance
r.sss.halfres=1; 1,0 for performance
r.sss.sampleset=2; 0,1,2 for performance
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
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=1; 0,1 for performance
r.supportexpfogmatchesvolumetricfog=1; 0,1 test
r.tessellationadaptivepixelspertriangle=48; 999999,48 for performance
r.translucency.autobeforedof=-1; -1,0.5 test
r.translucencylightingvolume.temporal=1; 0,1 test
r.translucencylightingvolumedim=48; 32,48,64 for performance
r.translucencyvolumeblur=1; 0 for performance
r.useparallelgetdynamicmeshelementstasks=1; 1,0 test
r.usepreexposure=0; test
r.vertexfoggingforopaque=1;
r.volumetriccloud.distancetosamplemaxcount=15;
r.volumetriccloud.enableatmosphericlightssampling=1;
r.volumetriccloud.enabledistantskylightsampling=1;
r.volumetriccloud.enablelocallightssampling=0; 0 for performance
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 0 for performance
r.volumetriccloud.shadow.viewraysamplemaxcount=9; 7,8,9,10,80 test
r.volumetriccloud.shadowmap.spatialfiltering=0; 0 for performance
r.volumetriccloud.shadowmap=0; 0 for performance
r.volumetriccloud.skyao=0;
r.volumetricfog.conservativedepth=0;
r.volumetricfog.depthdistributionscale=16; 16,32 test
r.volumetricfog.emissive=0; 0 for performance
r.volumetricfog.historymisssupersamplecount=2; 2 for performance
r.volumetricfog.historyweight=0.95; 0.9,0.95 test
r.volumetricfog.injectraytracedlights.locallights=0; 0 for performance
r.volumetricfog.injectshadowedlights=0; 0 for performance
r.volumetricfog.injectshadowedlightsseparately=0; 0,1 for performance
r.volumetricfog.lightfunction=0;
r.volumetricfog.lightsoftfading=0; test
r.volumetricfog.temporalreprojection=1;
r.volumetricfog.upsamplejittermultiplier=0; 0 for performance
r.volumetricfog.useslightfunctionatlas=1;
r.vrs.contrastadaptiveshading=1; test
r.vrs.decals=0;
r.vrs.enable=0;
r.vrs.enableimage=0;
r.vrs.enablesoftware=1;
r.vsync=0;
r.water.singlelayer.depthprepass=1;
r.water.singlelayer.distancefieldshadow=0; 0 for performance
r.water.singlelayer.refractiondownsamplefactor=1; 1,2 for performance
r.water.singlelayer.rtr=0;
r.water.singlelayer.shaderssupportdistancefieldshadow=0; 0 for performance
r.water.singlelayer.shaderssupportvsmfiltering=0; test
r.water.singlelayer.tiledcomposite=1;
r.water.singlelayer.underwaterfogwhencameraisabovewater=0;
r.water.singlelayer.vsmfiltering=0; test
r.water.watermesh.tessfactorbias=0; -1 for performance
rhi.maximumframelatency=1;
```

---

## open Input.ini and copy pasta %localappdata%

```python
[/script/engine.inputsettings]
baltentertogglesfullscreen=1;
benablemousesmoothing=0;
bf11togglesfullscreen=0;
buttonrepeatdelay=0.1;
bviewaccelerationenabled=0;
doubleclicktime=0.01; default is 0.1 test
initialbuttonrepeatdelay=0.1; default is 0.2 test
```

---

## ect

```python
## upscaling to use
2560x1440 use 58%,67%,70%,77% for performance (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3328x1872 use 50%,58%,67%,70%,77% for performance (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3840x2160 use 33%,50%,58%,67%,70%,77% for performance (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

## repak.bat method
zzz_inimods\engine\config\windows\windowsengine.ini
zzz_inimods\engine\config\windows\windowsinput.ini
```

---
