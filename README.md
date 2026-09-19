## updated 9/19/2026 ✂ 📋 🌀 :ramen: v1.5.1

### quality ue4/5 config and for reference/customization/optimization/learning

## open Engine.ini and copy pasta %localappdata% (make .ini's read only*)

#### check/change for performance options (left to right, performance to quality)

#### after pasting ini open game and change settings(low/med/high/ultra/vsync/switches) then restart game*

---

#### add after customizing
```python
perfindexvalues_resolutionquality="50 50 50 50 50"; test requires read only
r.mipmaplodbias=-1; -2.5,-2,-1.8,-1.6,-1.5,-1.4,-1,-0.5 for dlss
r.streaming.poolsize=4000; 400,600,800,1000,2000,3000,4000 to lower vram usage
sg.resolutionquality=50; 33,50,59,67,77,100
```
#### add after customizing 2
```python
d3d12.maximumframelatency=1; def 3 test
foliage.culldistancescale=0.85; 0.55,0.7,0.85,1 for performance test
foliage.minimumscreensize=0.000005; 0.000025,0.000015,0.000005 for performance test
fx.niagara.collision.cpuenabled=0; gpu dependent def 1 test
fx.niagara.qualitylevel=2; 0,1,2,3 for performance
grass.culldistancescale=0.85; 0.55,0.7,0.85,1 for performance test
r.allowhdr=0;
r.allowlandscapeshadows=1; 0 for performance
r.allowstaticlighting=0; def 1 test can cause crash
r.anisotropicmaterials=0; 0,1 for performance
r.antialiasingmethod=4; 0,1,2,3,4 off,fxaa,taa,msaa,tsr def 4
r.aoquality=1; 0,1,2 for performance
r.bloom.screenpercentage=50; 50,100 def 50
r.bloomquality=4;
r.capsuleshadows=0; 0,1 for performance
r.contactshadows=1; 0,1 for performance
r.defaultbackbufferpixelformat=4; 0,4 8bit,10bit def 4 for hdr test
r.defaultfeature.antialiasing=2; 0,1,2,3 off,fxaa,taa,msaa def 2
r.depthoffieldquality=2; 0,1,2,4 for performance def 2
r.detailmode=2; 0,1,2,3 for performance def 3
r.dfdistancescale=1.75; 1,1.75,2 def 1 test
r.dfshadowquality=3; 0,1,2,3 for performance def 3 test
r.disabledistortion=0; test
r.disablelandscapenanitegi=1; def 1
r.distancefieldao=1; 0 for performance
r.distancefieldshadowing=1; 0 for performance
r.dof.temporalaaquality=1; def 1 test
r.dynamicglobalilluminationmethod=1; 0 none 1 lumen 2 ssgi test
r.dynamicres.operationmode=0;
r.fastblurthreshold=3; 0,3,7,16,100 def 7
r.fog=1;
r.fullscreenmode=0; 0,1 fullscreen,windowed
r.fxaa.quality=0; 0,1,2,3,4,5 def 4
r.hairstrands.skyao=0; 0,1 def 1 test
r.hdr.enablehdroutput=0;
r.heterogeneousvolumes=0; 0,1 test can cause crash
r.hzbocclusion=1; scene depended test can cause crash
r.lensflarequality=2; 0,1,2
r.lightshaftquality=1; 0,1 def 1
r.lumen.diffuseindirect.allow=1; test
r.lumen.diffuseindirect.ssao=0; def 0 test
r.lumen.heightfog=0; def 1 test
r.lumen.heightfogongi=0; def 0
r.lumen.reflections.allow=1; test
r.lumen.reflections.temporal=0; def 1 test
r.lumen.reflections.tracemeshsdfs=0; 0 for performance def 1 test
r.lumen.screenprobegather.temporal.distancethreshold=0.015; 0.015,0.005 test
r.lumen.screenprobegather.temporalfilterprobes=1; def 0 test
r.lumen.tracemeshsdfs.allow=0; 0,1 for performance def 1
r.lumen.translucencyreflections.frontlayer.allow=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enableforproject=0; 0 for performance
r.materialqualitylevel=1; 0,2,1,3 for performance
r.maxanisotropy=16; 0,4,8 for performance
r.megalights.allowed=0; test
r.megalights.enableforproject=0; test
r.minscreenradiusforlights=0.03; 0.12,0.1,0.08,0.06,0.05,0.04,0.03,0.015 for performance test
r.motionblurquality=0; def 4
r.nanite.allowtessellation=0; def 0 test can cause crash
r.nanite.meshshaderrasterization=1; def 1 test
r.nanite.tessellation=0; def 0 test can cause crash
r.ngx.dlss.quality.auto=0; 0 for performance
r.ngx.dlss.reflections.temporalaa=0; def 1 test
r.ngx.dlss.waterreflections.temporalaa=0; def 0 test
r.particlelightquality=1; 0,1,2 for performance
r.postprocessaaquality=6; 0 off 1,2 fxaa 3,4,5,6 taa
r.reflectionmethod=1; 0 none 1 lumen 2 ssr test
r.reflections.denoiser.temporalaccumulation=0; def 1 test
r.refraction.blur.temporalaa=1; def 1
r.refractionquality=1; 0,1,2 for performance
r.shadow.maxcsmresolution=2048; 1024,2048 for performance
r.shadow.maxresolution=1024; 1024,2048 for performance
r.shadow.radiusthreshold=0.02; 0.06,0.05,0.04,0.03,0.02,0.01 for performance
r.shadow.virtual.enable=1; 0 for performance
r.shadow.virtual.forceonlyvirtualshadowmaps=1; test
r.shadowquality=3; 3,4,5 for performance
r.ssgi.quality=0; 0,2,3 for performance
r.ssr.quality=2; 0,2,3 for performance
r.ssr.temporal=1;
r.supportlocalfogvolumes=0; def 1 test
r.supportmateriallayers=1; 0,1 for performance
r.temporalaa.algorithm=1; 0,1 for gen4,gen5 test
r.temporalaa.quality=2; 1,2 for performance def 2 test
r.temporalaa.upsampling=1; def 1
r.temporalaacurrentframeweight=0.04; def 0.04
r.temporalaafiltersize=1; def 1 test
r.temporalaasamples=8; 8,16 test
r.tessellationadaptivepixelspertriangle=48; 999999,48 for performance
r.tonemapper.quality=5; 0,2,5
r.tonemapper.sharpen=1; 0,1,2
r.translucencylightingvolume.temporal=1; 0,1 test
r.tsr.history.screenpercentage=100; def 200 test
r.upscale.quality=2; 0,1,2,3,4 def 3
r.volumetriccloud.shadowmap=1; 0 for performance def 1 test
r.volumetriccloud.skyao=0; def 1
r.volumetriccloud=1; 0,1 for performance
r.volumetricfog.temporalreprojection=1; def 1
r.vrs.enable=0; def 0 test
r.vrs.enablesoftware=0; def 0 test
r.vsync=0;
r.water.enableshallowwatersimulation=0; 0 for performance test
r.water.enableunderwaterpostprocess=1; 0,1 for performance test
r.water.singlelayer.reflection=3; 0,2,3,1 test
r.water.singlelayer.ssr=1; 0,1 for performance
r.water.singlelayer=1; def 1
rhi.maximumframelatency=1; def 3 test
t.maxfps=-1;
t.streamline.reflex.enable=1;
```
#### add after customizing ray tracing stuff
```python
r.hairstrands.raytracing=0; def 1
r.heterogeneousvolumes.hardwareraytracing=0; def 0
r.lumen.hardwareraytracing.avoidselfintersections=0; test
r.lumen.hardwareraytracing.farfieldbias=200; def 200
r.lumen.hardwareraytracing.hitlighting.reflectioncaptures=0; def 0
r.lumen.hardwareraytracing.inline=0; def 1 lumen hardwareraytracing switch test
r.lumen.hardwareraytracing.lightingmode=0; 0,1,2,3 def 0 test
r.lumen.hardwareraytracing.maxiterations=8192; def 8192
r.lumen.hardwareraytracing.mintracedistancetosamplesurfacecache=10;
r.lumen.hardwareraytracing.pullbackbias=8; def 8
r.lumen.hardwareraytracing.skipbackfacehitdistance=5; def 5
r.lumen.hardwareraytracing.skiptwosidedhitdistance=1; def 1
r.lumen.hardwareraytracing=0; def 0 test
r.lumen.radiancecache.hardwareraytracing.retrace.farfield=0; def 1 test
r.lumen.radiancecache.hardwareraytracing.temporarybufferallocationdownsamplefactor=8; def 8
r.lumen.radiancecache.hardwareraytracing=0; def 1 test
r.lumen.reflections.hardwareraytracing.bucketmaterials=1; 1 for performance def 1 test
r.lumen.reflections.hardwareraytracing.retrace.farfield=0; def 1 test
r.lumen.reflections.hardwareraytracing.retrace.hitlighting=0; def 0
r.lumen.reflections.hardwareraytracing.translucent.maxrefractionbounces=0; def 0
r.lumen.reflections.hardwareraytracing.translucent.refraction.enableforproject=0; 0 for performance def 1 test
r.lumen.reflections.hardwareraytracing=0; def 1 test
r.lumen.screenprobegather.hardwareraytracing.retrace.farfield=0; def 1 test
r.lumen.screenprobegather.hardwareraytracing=0; def 1 test
r.lumen.screenprobegather.shortrangeao.hardwareraytracing=0; def 0
r.lumen.translucencyvolume.hardwareraytracing=0; def 1 test
r.lumenscene.directlighting.hardwareraytracing.forcetwosided=0; def 0
r.lumenscene.directlighting.hardwareraytracing=0; def 1 test
r.lumenscene.farfield.maxtracedistance=1000000; test
r.lumenscene.farfield=0; 0,1 test
r.lumenscene.radiosity.hardwareraytracing=0; def 1 test
r.manylights.hardwareraytracing=0; def 1 test
r.megalights.hardwareraytracing.farfield=0; def 0
r.ngx.dlss.denoisermode=0; ray reconstruction test can cause crash
r.pathtracing=0;
r.raytracing.ambientocclusion=0;
r.raytracing.culling.radius=30000; test
r.raytracing.enable=0; 0 disables lumen hardwareraytracing
r.raytracing.enableingame=0; 0 disables lumen hardwareraytracing
r.raytracing.enableondemand=0;
r.raytracing.excludedecals=1; def 0 test
r.raytracing.excludesky=1; def 1
r.raytracing.excludetranslucent=0; def 0
r.raytracing.forceallraytracingeffects=0;
r.raytracing.globalillumination=0;
r.raytracing.lightfunction=0;
r.raytracing.raytracingproxies.projectenabled=1; 1 for performance
r.raytracing.reflections=0;
r.raytracing.scene.buildmode=1; 0,1 test
r.raytracing.shadows=0;
r.raytracing.skylight=0;
r.raytracing.translucency=0;
r.raytracing.usetexturelod=0; 0,1 test
r.raytracing=0; 0 disables lumen hardwareraytracing
r.volumetricfog.injectraytracedlights=0; def 0
```

---

## base config:

```python
[core.log]
global=off;

[crashreportclient]
ballowtobecontacted=0;
bisallowedtoclosewithoutsending=1;
bisallowedtosendwithoutdetailedinfo=0;
bsendlogfile=0;
bsendunattendedbugreports=0;
cansendwhenuifailedtoinitialize=0;
datarouterurl=;
ensure.recorddump=0;
stall.recorddump=0;
uiinitretrycount=0;

[gametelemetry]
authenticationkey=;
configkey=;
configurl=;
ingesturl=;
logwarnings=;
maxbuffersize=;
maxcountpermessage=;
maxuniquemessages=;
querytakelimit=;
queryurl=;
sendinterval=;

[/script/engine.engine]
bpauseonlossoffocus=0;
bsmoothframerate=0;
busefixedframerate=0;

[texturestreaming]
poolsizevrampercentage=70; 50 to lower vram usage

[consolevariables]
d3d12.adjusttexturepoolsizebasedonbudget=0; 1 is experimental test
d3d12.syncwithdwm=0; def 0
foliage.minlod=-1; def -1
foliage.minocclusionqueriespercomponent=2; 6,2 test
fx.allowgpusorting=1;
fx.batchasyncbatchsize=32; 16,32,64 test
fx.niagaraallowgpuparticles=1;
fx.niagaraallowruntimescalabilitychanges=1;
fx.qualitylevelspawnratescalereferencelevel=2; test
grass.disabledynamicshadows=0; 1 for performance
grass.tickinterval=1; def 1
health.loghealthsnapshot=0; def 1 test
r.allowsubprimitivequeries=1; def 1
r.ambientocclusion.compute.smooth=1; test
r.ambientocclusion.compute=0; test
r.ambientocclusion.method=0;
r.ambientocclusionlevels=-1; 0,1,2 for performance def -1
r.ambientocclusionmaxquality=100; -60,100 test
r.ambientocclusionmiplevelfactor=1;
r.ambientocclusionradiusscale=1; 0.85,1 test
r.ambientocclusionstaticfraction=-1; 0,1 for performance def -1
r.aoapplytostaticindirect=0; def 0 test
r.aoglobaldistancefield.mipfactor=4; 8,4 for performance
r.aoglobaldistancefield=1; def 1
r.aoglobaldistancefieldclipmapupdatesperframe=1; def 2 test
r.aoglobaldistancefieldrepresentheightfields=1;
r.aohistorydistancethreshold=60; 60,30 test
r.aohistoryweight=0.85; 0.85,0.95 test
r.aomaxviewdistance=10000; 10000,20000 is 100m,200m def 20000 test
r.aospecularocclusionmode=0; 0,1 test
r.aoviewfadedistancescale=0.7; 0.7 test
r.blurgbuffer=-1; 0,-1 def -1
r.capsuleshadowsfullresolution=0; def 0
r.chaos.reflectioncapturestaticsceneonly=1; def 1
r.compileshadersfordevelopment=0; def 1
r.contactshadows.overrideshadowcastingintensity=50; def -1 test
r.contactshadows.standalone.method=0; def 0 test
r.d3d.forcedxc=0; multigpu def 0
r.d3d11.depth24bit=0; 1 for performance
r.d3d11.useallowtearing=1;
r.d3d12.depth24bit=0; 1 for performance
r.d3d12.gpucrashdebuggingmode=0;
r.d3d12.shadowdepth32bit=0; 0 for performance
r.d3d12.useallowtearing=1;
r.decal.fadedurationscale=1; def 1 test
r.decal.fadescreensizemult=1; def 1
r.decal.stencilsizethreshold=0.1; def 0.1
r.detectandwarnofbaddrivers=0;
r.dffullresolution=0; 0 for performance
r.diffuseindirect.halfres=1; def 1
r.distancefields.brickatlasmaxsizez=16; def 32 test
r.distancefields.maxpermeshresolution=128; 128,256 to lower vram usage
r.dof.gather.accumulatorquality=0; 0,1 def 1
r.dof.gather.enablebokehsettings=0; 0,1 def 1
r.dof.gather.postfiltermethod=1; 0,1,2 def 1
r.dof.gather.resolutiondivisor=2; 2,1 def 2
r.dof.gather.ringcount=4; 3,4,5 def 4
r.dof.kernel.maxbackgroundradius=0.012; 0.012,0.025 def 0.025
r.dof.kernel.maxforegroundradius=0.012; 0.012,0.025 def 0.025
r.dof.recombine.enablebokehsettings=0; 0,1 def 1
r.dof.recombine.quality=0; 0,1,2 def 2
r.dof.scatter.backgroundcompositing=1; 0,1,2 def 2
r.dof.scatter.enablebokehsettings=0; 0,1 def 1
r.dof.scatter.foregroundcompositing=1; 0,1 def 1
r.dof.scatter.maxspriteratio=0.04; 0.04,0.1,0.25 def 0.1
r.emitter.fastpoolenable=1;
r.emitter.fastpoolmaxfreesize=4194304; 2097152,4194304 test
r.emitterspawnratescale=1; 0.125,0.25,0.5,1 for performance
r.filmgrain=0;
r.filter.loopmode=0; def 0 test
r.filter.sizescale=1; def 1
r.finishcurrentframe=0; 1 for latency cost too much
r.forcedebugviewmodes=0;
r.forwardshading.forceskylightcubemapblending=0; 0 for performance test
r.gbufferdiffusesampleocclusion=0; 0,1 for performance
r.gpucrash.collectionenable=0;
r.gtsynctype=0;
r.hairstrands.composeaftertranslucency=1;
r.hairstrands.deepshadow.supersampling=0;
r.hairstrands.dofdepth=0; def 1 test
r.hairstrands.interpolation.usesingleguide=1; 1,0 for performance def 1
r.hairstrands.minlod=0;
r.hairstrands.rasterizationscale=0.5;
r.hairstrands.scatterscenelighting=1; def 1 test
r.hairstrands.shadow.castshadowwhennonvisible=0; 0 for performance def 1 test
r.hairstrands.skyao.samplecount=2; 2,4 def 4 test
r.hairstrands.skylighting.integrationtype=2;
r.hairstrands.skylighting.jitterintegration=0; 0 for performance test
r.hairstrands.skylighting.screentraceocclusion=0; 0 for performance test
r.hairstrands.usecardsinsteadofstrands=0; 1 for performance
r.hairstrands.velocityrasterizationscale=0.5; 0.5,1,1.5 for performance
r.hairstrands.visibility.msaa.sampleperpixel=1; 1,2,4 for performance
r.hairstrands.visibility.ppll=0;
r.heterogeneousvolumes.downsamplefactor=2; 8,4,2,1 for performance test
r.heterogeneousvolumes.heightfog=0; def 1 test
r.heterogeneousvolumes.maxstepcount=256; 128,256,512 for performance test
r.heterogeneousvolumes.shadows.resolution=256; 128,256,512 for performance test
r.irisnormal=0; def 0 test
r.landscapelodbias=0; 1 for performance
r.lightfunctionquality=1; 1,2 for performance
r.lightmaxdrawdistancescale=1; 0.6,0.85,1 for performance
r.localfogvolume.renderduringheightfogpass=0; def 0 test
r.lumen.reflections.bilateralfilter=0; 0,1 for performance def 1
r.lumen.reflections.distantscreentraces=0; 0 for performance def 1 test
r.lumen.reflections.downsamplecheckerboard=0; def 0 test
r.lumen.reflections.downsamplefactor=1; 2,1 for performance def 1 test
r.lumen.reflections.hairstrands.screentrace=0; test
r.lumen.reflections.hairstrands.voxeltrace=0; test
r.lumen.reflections.hierarchicalscreentraces.maxiterations=50;
r.lumen.reflections.hierarchicalscreentraces.minimumoccupancy=0;
r.lumen.reflections.hiressurface=0; 0 for performance def 1
r.lumen.reflections.maxbounces=0; 0,1,2 to 8 to 64 for performance test
r.lumen.reflections.maxroughnesstotrace=0.1; 0.1 for performance def -1 test
r.lumen.reflections.maxroughnesstotraceclamp=0.1; 0.1 for performance def 1 test
r.lumen.reflections.maxroughnesstotraceforfoliage=0; 0 for performance def 0.4 test
r.lumen.reflections.radiancecache=1; def 0 test
r.lumen.reflections.roughnessfadelength=0.1; test
r.lumen.reflections.samplescenecolorathit=1; 0,1,2 for performance def 1 test
r.lumen.reflections.screenspacereconstruction.tonemapstrength=0; def 0
r.lumen.reflections.screenspacereconstruction=1; def 1 test
r.lumen.reflections.screentraces=1; def 1 test
r.lumen.reflections.smoothbias=0; 0 for performance def 0 test
r.lumen.reflections.specularscale=1; test
r.lumen.screenprobegather.downsamplefactor=16; 32,16 for performance def 16
r.lumen.screenprobegather.fullresolutionjitterwidth=1; 0.25 to 8 def 1 test
r.lumen.screenprobegather.importancesample=1; 0 for performance def 1 test
r.lumen.screenprobegather.integratedownsamplefactor=1; 2,1 for performance def 1 test
r.lumen.screenprobegather.irradianceformat=0; test
r.lumen.screenprobegather.materialao=1; test
r.lumen.screenprobegather.radiancecache.numprobestotracebudget=300; 150,200,300 def 300 test
r.lumen.screenprobegather.radiancecache.proberesolution=16; 8,16,32 for performance def 32
r.lumen.screenprobegather.screenspacebentnormal=1; def 1 test
r.lumen.screenprobegather.screentraces.hzbtraversal.fullresdepth=0; def 1 test
r.lumen.screenprobegather.screentraces=0; def 1 test
r.lumen.screenprobegather.shortrangeao.bentnormal=1; 0 for performance def 1 test
r.lumen.screenprobegather.shortrangeao.hairscreentrace=0; test
r.lumen.screenprobegather.shortrangeao.hairvoxeltrace=0; 0 for performance def 1 test
r.lumen.screenprobegather.shortrangeao=1; def 1 test
r.lumen.screenprobegather.stochasticinterpolation=1; 1,0 for performance def 0
r.lumen.screenprobegather.tracingoctahedronresolution=8; 8,16 def 8 test
r.lumen.screenprobegather.twosidedfoliagebackfacediffuse=0; 0,1 for performance def 1 test
r.lumen.tracemeshsdfs=0; 0 for performance def 0 test
r.lumen.translucencyvolume.enable=1; def 1
r.lumen.translucencyvolume.enddistancefromcamera=2000; 500,1000,2000,3000 def 8000 test
r.lumen.translucencyvolume.gridpixelsize=64; 128,64,32 for performance def 32 test
r.lumen.translucencyvolume.radiancecache.gridresolution=24; 12,24 for performance def 24 test
r.lumen.translucencyvolume.radiancecache.nummipmaps=1; def 3 test
r.lumen.translucencyvolume.radiancecache.numprobestotracebudget=150; 100,125,150,175 def 200 test
r.lumen.translucencyvolume.radiancecache.probeatlasresolutioninprobes=128; def 128
r.lumen.translucencyvolume.radiancecache=1; 0 for performance def 1 test
r.lumen.translucencyvolume.spatialfilter.mode=1; def 1
r.lumen.translucencyvolume.spatialfilter.numpasses=2; def 2
r.lumen.translucencyvolume.spatialfilter.samplecount=3; def 3
r.lumen.translucencyvolume.spatialfilter.standarddeviation=5; def 5
r.lumen.translucencyvolume.spatialfilter=1; 0,1,2 def 1 test
r.lumen.translucencyvolume.tracefromvolume=1; 0 for performance def 1 test
r.lumenscene.directlighting.maxlightspertile=8; 4,8 for performance def 8 test
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0; 0 for performance def 1 test
r.lumenscene.directlighting.updatefactor=32; 64,32 for performance def 32 test
r.lumenscene.globalsdf.notcoveredexpandsurfacescale=0.7; def 0.6 test
r.lumenscene.radiosity.hemisphereproberesolution=3; 2,3,4 for performance def 4
r.lumenscene.radiosity.probespacing=8; 16,8,4 for performance def 4
r.lumenscene.radiosity.updatefactor=128; 128,64 def 64 test
r.lumenscene.radiosity=1; 0,1 for performance def 1
r.lumenscene.surfacecache.atlassize=2048; def 4096 test
r.lumenscene.surfacecache.cardcapturerefreshfraction=0.0625; 0,0.03125,0.0625,0.125 def 0.125
r.lumenscene.surfacecache.cardmaxresolution=64; def 512 test
r.lumenscene.surfacecache.cardmaxtexeldensity=0.05; def 0.2 test
r.lumenscene.surfacecache.cardminresolution=1; def 4 test
r.lumenscene.surfacecache.cardtexeldensityscale=25; def 100 test
r.materiallogerroronfailure=0;
r.minroughnessoverride=0; def 0
r.motionblur.halfresgather=0; 1,0 def 0
r.motionblur.halfresinput=1; def 1
r.motionblurscatter=0; 0,1 def 0
r.motionblurseparable=0; 0,1 def 0
r.nanite.allowskinnedmeshes=1; 0,1 test
r.nanite.computerasterization=1; 1 for performance def 1 test
r.nanite.decompressdepth=0; 1 for performance def 0 test
r.nanite.dicingrate=4; 4,2 for performance def 2 test
r.nanite.maxcandidateclusters=3145728; test
r.nanite.maxcandidatepatches=262144; 262144,2097152 test
r.nanite.maxpixelsperedge=3; 4,3.5,3,2.5,1 for performance
r.nanite.maxpixelsperedgeheavygeometry=2; 2.3,2.15,2,1.75,1 test
r.nanite.maxpixelsperedgelowgeometry=3.5; 6,4.5,3.5,2.5,1 test
r.nanite.maxvisibleclusters=1572864; test
r.nanite.maxvisiblepatches=65536; 65536,655360,2097152 test
r.nanite.shadowraster.minpixelradius=16; 32,24,16,8,0 for performance test
r.nanite.softwarevrs=1; def 1
r.nanite.streaming.imposters=0; def 1 test
r.nanite.streaming.reservedresources=1; 1 is experimental test
r.nanite.usepregeneratedinstancesbuffer=0; def 0 test
r.nanite.viewmeshlodbias.min=-2;
r.nanite.viewmeshlodbias.offset=0;
r.ngx.dlss.prefernissharpen=0;
r.ngx.dlss.sharpness=0.5;
r.ngx.loglevel=0;
r.nis.enable=0;
r.nis.sharpness=0;
r.numbufferedocclusionqueries=1; test
r.oneframethreadlag=1; 0 for latency cost too much
r.postprocessing.prefercompute=0; gpu dependent def 0 test
r.postprocessing.quarterresolutiondownsample=0; 1 for performance def 0
r.reflectioncapturesupersamplefactor=1; 1 for performance
r.refraction.blur=0; def 1 test
r.refraction.offsetquality=1; test
r.rendertargetpoolmin=450; 200,400,450 to lower vram usage
r.rhicmdbypass=0;
r.scenecolorformat=3; 2,3,4 for performance
r.scenecolorfringe.max=0;
r.scenecolorfringequality=0; 0,1
r.sceneculling.explicitcellbounds=0; 0 for performance
r.screenpercentage.maxresolution=0;
r.screenpercentage.minresolution=0;
r.secondaryscreenpercentage.gameviewport=0;
r.shaders.removedeadcode=1;
r.shaders.removeunusedinterpolators=1;
r.shadow.csm.maxcascades=2; 2,4,10 for performance
r.shadow.csm.transitionscale=1;
r.shadow.csmshadowdistancefadeoutmultiplier=1;
r.shadow.cullminorshadowcasters=0; 0,1 for performance
r.shadow.detectvertexshaderlayeratruntime=1; def 1
r.shadow.forcesinglesampleshadowingfromstationary=0;
r.shadow.itemlightcomponentshadows=1; 0,1 for performance
r.shadow.nanitelodbias=0; 2,1,0 for performance test
r.shadow.preshadowresolutionfactor=0.5; 0.5,1 for performance
r.shadow.scene.lightactiveframecount=10; def 10 test
r.shadow.unbuiltpreviewingame=0; def 1
r.shadow.virtual.cache.forceinvalidatedirectional=0; def 0
r.shadow.virtual.markpixelpagesmipmodelocal=2; 2,1,0 for performance test
r.shadow.virtual.maxphysicalpages=2048; 512,1024,2048,4096 to lower vram usage test
r.shadow.virtual.nonnanite.includeincoarsepages=0; 0,1 for performance
r.shadow.virtual.nonnanite.usehzb=2; def 2
r.shadow.virtual.onepassprojection.maxlightsperpixel=8; 4,8,16,32 for performance
r.shadow.virtual.onepassprojection=1; 1 for performance
r.shadow.virtual.resolutionlodbiasdirectional=-0.75; -0.5,-0.75,-1,-1.5 def -1.5 test
r.shadow.virtual.resolutionlodbiasdirectionalmoving=-0.75; -0.5,-0.75,-1,-1.5 def -1.5 test
r.shadow.virtual.resolutionlodbiaslocal=0; 3,2,1,0 for performance def 0 test
r.shadow.virtual.resolutionlodbiaslocalmoving=1; 3,2,1 for performance def 1 test
r.shadow.virtual.smrt.adaptiveraycount=1; def 1
r.shadow.virtual.smrt.extrapolatemaxslopelocal=0; 0 for performance def 0.05 test
r.shadow.virtual.smrt.raycountdirectional=3; 0,2,3,4,8 def 8 test
r.shadow.virtual.smrt.raycountlocal=2; 0,2,3,4,8 def 8 test
r.shadow.virtual.smrt.raylengthscaledirectional=0.4; def 1.5 test
r.shadow.virtual.smrt.samplesperraydirectional=2; 1,2,4 test
r.shadow.virtual.smrt.samplesperraylocal=2; 0,1,2,4 def 4 test
r.shadow.virtual.smrt.texelditherscaledirectional=2; def 2 test
r.shadow.virtual.smrt.texelditherscalelocal=2; 2,4,6 def 2 test
r.shadow.virtual.translucentquality=0; 0 for performance test
r.shadow.virtual.usehzb=2; def 2
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
r.splinemesh.norecreateproxy=1; def 1
r.ssr.compute=1; def 0 test
r.ssr.halfresscenecolor=1; 1,0 for performance
r.ssr.maxroughness=0.95; 0.95,1 def -1 test
r.ssr.tiledcomposite=0; test
r.sss.burley.bilateralfilterkernelfunctiontype=1; 1,0 for performance
r.sss.burley.quality=1; 0,1 for performance
r.sss.checkerboard=2; 1,2,0 for performance
r.sss.halfres.forceseparable=1; 1,0 for performance
r.sss.halfres=1; 1,0 for performance
r.sss.quality=1; 0,-1,1 for performance
r.sss.sampleset=1; 0,1,2 for performance
r.sss.scale=0.75; 0,0.75,1 test
r.streaming.amortizecputogpucopy=0;
r.streaming.boost=1;
r.streaming.dropmips=0; 1 to lower vram usage
r.streaming.fullyloadmeshes=0;
r.streaming.fullyloadusedtextures=0;
r.streaming.hiddenprimitivescale=0.5; 0,0.25,0.5 for performance
r.streaming.limitpoolsizetovram=0; 0 to manually set poolsize
r.streaming.maxeffectivescreensize=0;
r.streaming.maxnumtexturestostreamperframe=0;
r.streaming.maxtempmemoryallowed=100; 50,75,100 to lower ram usage
r.streaming.mipbias=0; 1 for performance
r.streaming.poolsize.vrampercentageclamp=1024;
r.streaming.poolsizeformeshes=-1;
r.streaming.useallmips=0;
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=1; def 1 test
r.subsurfacescattering=1; 0 for performance
r.supportexpfogmatchesvolumetricfog=0; def 0 test
r.translucency.autobeforedof=-1; -1,0.5 test
r.translucencylightingvolumedim=48; 32,48,64 for performance
r.translucencyvolumeblur=1; def 1
r.translucentlightingvolume=1; 0 for performance def 1
r.useparallelgetdynamicmeshelementstasks=1; 1,0 test
r.usepreexposure=0; test
r.vertexfoggingforopaque=1; def 1
r.virtualtexturereducedmemory=1; 1 to lower vram usage
r.volumetriccloud.distancetosamplemaxcount=23; 30,25,23,20,15 test
r.volumetriccloud.enableatmosphericlightssampling=1; def 1
r.volumetriccloud.enabledistantskylightsampling=1; def 1
r.volumetriccloud.enablelocallightssampling=0; 0 for performance
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 0 for performance
r.volumetriccloud.shadow.viewraysamplemaxcount=9; 7,8,9,10,80 test
r.volumetriccloud.shadowmap.spatialfiltering=1; 0,1,2,3,4 def 1
r.volumetriccloud.viewraysamplemaxcount=256; 128,256,768 test
r.volumetricfog.conservativedepth=0;
r.volumetricfog.depthdistributionscale=32; 16,32 def 32 test
r.volumetricfog.distanceoverride=12000; 12000 is 120m def -1 test
r.volumetricfog.emissive=0; 0 for performance def 1
r.volumetricfog.historymisssupersamplecount=2; 2,4,8 for performance test
r.volumetricfog.historyweight=0.9; 0.9,0.95 test
r.volumetricfog.injectshadowedlights=1; def 1 test
r.volumetricfog.injectshadowedlightsseparately=1; def 1 test
r.volumetricfog.lightfunction=1; def 1 test
r.volumetricfog.lightsoftfading=1; def 1 test
r.volumetricfog.upsamplejittermultiplier=0; 0 for performance
r.volumetricfog.useslightfunctionatlas=1;
r.volumetricfog=1; 0,1 for performance
r.vrs.basepass=2; def 2
r.vrs.contrastadaptiveshading=0; def 0
r.vrs.decals=2; def 2
r.vrs.enableimage=0; def 0
r.vrs.lightfunctions=1; def 1
r.vrs.naniteemitgbuffer=2; def 2
r.vrs.reflectionenvironmentsky=2; def 2
r.vrs.ssao=0; def 0
r.vrs.ssr=2; def 2
r.vrs.translucency=1; def 1
r.vt.anisotropicfiltering=1; 0 for performance
r.vt.maxanisotropy=8; 2,4,8 for performance
r.vt.numgathertasks=4; 1,2,4,8 cpu dependent test
r.vt.poolsizescale=1; 1,2,4,8 to lower vram usage
r.water.singlelayer.depthprepass=0; def 1
r.water.singlelayer.distancefieldshadow=0; def 1 test
r.water.singlelayer.refractiondownsamplefactor=1; 1,2 for performance
r.water.singlelayer.rtr=0;
r.water.singlelayer.shaderssupportdistancefieldshadow=0; def 1 test
r.water.singlelayer.shaderssupportvsmfiltering=0; test
r.water.singlelayer.tiledcomposite=1;
r.water.singlelayer.underwaterfogwhencameraisabovewater=0;
r.water.singlelayer.vsmfiltering=0; test
r.water.singlelayerwater.supportcloudshadow=1; def 0 test
rhi.syncslackms=0;
t.streamline.reflex.mode=2; 0,1,2
```

---

## optional async

#### optional async test skip unless you are testing
```python
fx.batchasync=1; def 0 test
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
#### optional async defaults test skip unless you are testing
```python
allowasyncrenderthreadupdates=1; def 1 test
allowasyncrenderthreadupdatesduringgamethreadupdates=1; def 1 test
d3d12.asyncdeferreddeletion=1; def 1 test
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

## open Input.ini and copy pasta %localappdata%

```python
[/script/engine.inputsettings]
baltentertogglesfullscreen=1;
benablemousesmoothing=0;
bf11togglesfullscreen=0;
bviewaccelerationenabled=0;

optional
buttonrepeatdelay=0.1;
doubleclicktime=0.01; def is 0.1 test
initialbuttonrepeatdelay=0.1; def is 0.2 test
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
