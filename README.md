## updated 10/3/2026 ✂ 📋 🌀 :ramen: v1.6.5

#### quality ue4/5 config and for reference/customization/optimization/learning

#### open/create Engine.ini and copy pasta %localappdata% (make read only*)

#### check/change "for performance" options (left to right, performance to quality)

#### after pasta open game and change graphics to your spec then restart game*

#### recommended* to delete %localappdata%\nvidia\dxcache and %localappdata%\d3dscache

---

```python
;vram poolsize customize (add under base config)
r.streaming.poolsize=3000; 400,600,800,1000,2000,3000 to lower vram usage

;match perfindexvalues/dlss.quality/resolutionquality customize (add under base config)
perfindexvalues_resolutionquality="50 50 50 50 50"; 33,50,59,67,77,100
r.mipmaplodbias=-0.5; -2.5,-2,-1.8,-1.6,-1.5,-1.4,-1,-0.5,0
r.ngx.dlss.quality=-1; -2,-1,0,1,2 ultra performance,performance,balanced,quality,ultra quality
sg.resolutionquality=50; 33,50,59,67,77,100

;customize (add under base config)
r.antialiasingmethod=2; 0,1,2,3,4 off,fxaa,taa,msaa,tsr def 4
r.defaultfeature.antialiasing=2; 0,1,2,3 off,fxaa,taa,msaa def 2
r.dof.temporalaaquality=1; def 1 test
r.dynamicres.changepercentagethreshold=1; 1,2 def 2 test
r.dynamicres.cpuboundscreenpercentage=100; def 100 test
r.dynamicres.dynamicframetime.errormarginpercent=5; 5,10 def 10 test
r.dynamicres.dynamicframetime=0; def 1 test
r.dynamicres.frametimebudget=16.6; 16.6,33.3 def 33.3
r.dynamicres.historysize=16; def 16 test
r.dynamicres.maxscreenpercentage=100; def 100
r.dynamicres.minresolutionchangeperiod=4; 4,8 def 8 test
r.dynamicres.minscreenpercentage=50; def 50
r.dynamicres.operationmode=0; def 0 test
r.dynamicres.targetedgpuheadroompercentage=3; 3,10 def 10 test
r.fxaa.quality=0; 0,1,2,3,4,5 def 4
r.lumen.reflections.temporal=0; def 1 test
r.lumen.screenprobegather.temporal.distancethreshold=0.005; 0.015,0.005 def 0.005 test
r.lumen.screenprobegather.temporal.maxframesaccumulated=10; def 10 test
r.lumen.screenprobegather.temporal=1; def 1
r.lumen.screenprobegather.temporalfilterprobes=0; def 0 test
r.msaa.compositingsamplecount=1;
r.msaacount=0;
r.postprocessaaquality=6; 0 off 1,2 fxaa 3,4,5,6 taa
r.reflections.denoiser.temporalaccumulation=0; def 1 test
r.refraction.blur.temporalaa=0; def 1 test
r.refraction.blur=0; def 1 test
r.screenpercentage.default=100; def 100
r.screenpercentage.maxresolution=0; def 0
r.screenpercentage.minresolution=0; def 0
r.secondaryscreenpercentage.gameviewport=0; 83.33,86.66 def 0 test
r.ssr.temporal=1; def 1
r.temporalaa.algorithm=0; 0,1 for gen4,gen5 test
r.temporalaa.historyscreenpercentage=100; def 100 test
r.temporalaa.quality=1; 1,2,3 def 2 test
r.temporalaa.upsampling=1; def 1 test
r.temporalaa.upscaler=1; def 1
r.temporalaacurrentframeweight=0.04; def 0.04 test
r.temporalaafiltersize=1; def 1 test
r.temporalaasamples=8; 8,16 test
r.translucencylightingvolume.temporal=0; def 0
r.translucencyvolumeblur=1; def 1
r.tsr.16bitvalu.nvidia=1; def 0 test
r.tsr.history.samplecount=16; 8,16,32 def 16 test
r.tsr.history.screenpercentage=100; 100,150 def 200 test
r.tsr.velocity.weightclampingsamplecount=4; def 4 test
r.volumetricfog.temporalreprojection=1; def 1
r.water.singlelayer.ssrtaa=1; def 1

;scaling stuff test (add under base config)
r.ngx.dlaa.enable=0;
r.ngx.dlss.autoexposure=1; def 1
r.ngx.dlss.builtindenoiseroverride=-1; def -1
r.ngx.dlss.enable=1;
r.ngx.dlss.prefernissharpen=0; 0,1,2 def 1
r.ngx.dlss.quality.auto=0;
r.ngx.dlss.reflections.temporalaa=0; def 1 test
r.ngx.dlss.sharpness=0; def 0 test
r.ngx.dlss.waterreflections.temporalaa=0; def 0 test
r.ngx.enable=1;
r.ngx.enableotherloggingsinks=0; def 0
r.ngx.loglevel=0; def 1 test
r.ngx.renamengxlogseverities=1; def 1
r.nis.enable=0;
r.nis.halfprecision=-1; def -1
r.nis.hdrmode=-1;
r.nis.sharpness=0; def 0
r.nis.upscaling=0;
r.streamline.deepdvc.enable=0;
r.streamline.dlssg.checkstatusperframe=1; def 1 test
r.streamline.initializeplugin=1;
r.streamline.load.deepdvc=0; def 1 test
r.streamline.load.dlssg=1;
r.streamline.load.reflex=1
r.streamline.logfunctions.loglevel=0;
r.streamline.logfunctions=0;
t.streamline.reflex.auto=1; def 1
t.streamline.reflex.enable=1;
t.streamline.reflex.handlemaxtickrate=0; def 1 test
t.streamline.reflex.mode=2; 0,1,2

;can cause crash in some games (add under base config)
r.allowstaticlighting=0; def 1
r.hzbocclusion=0; def 0
r.nanite.allowtessellation=0; def 0
r.nanite.tessellation=0; def 0
r.ngx.dlss.denoisermode=0; ray reconstruction test

;latency customize (add under base config)
d3d12.maximumframelatency=1; def 3 test
r.d3d11.useallowtearing=1; def 0
r.d3d12.useallowtearing=1; def 1
r.finishcurrentframe=0; 1 for latency cost too much
r.fullscreenmode=0; 0,1 fullscreen,windowed
r.gtsynctype=0; 2,1,0 def 0 test
r.numbufferedocclusionqueries=1; def 1 test
r.oneframethreadlag=1; 0 for latency cost too much
r.vsync=0; def 0
rhi.maximumframelatency=1; def 3 test
rhi.syncinterval=0; 1,0 def 1 test
rhi.syncslackms=0; def 10
t.maxfps=0; def 0
t.overridefps=0; def 0
t.unsteadyfps=0; def 0

;optional quality customize test (add under base config)
foliage.culldistancescale=0.85; 0.7,0.85,1 for performance
foliage.densityscale=0.6; 0.6,0.7,1 for performance
foliage.minlod=-1; def -1
foliage.minocclusionqueriespercomponent=6; def 6
grass.culldistancescale=0.85; 0.7,0.85,1 for performance
grass.densityscale=0.6; 0.6,0.7,1 for performance
grass.disabledynamicshadows=0; 1 for performance
r.dfdistancescale=1; 1,1.5,1.75,2,3,3.5 def 1 test
r.lightmaxdrawdistancescale=1; 0.6,0.85,1 for performance
r.minscreenradiusforlights=0.02; 0.12,0.1,0.08,0.06,0.05,0.04,0.03,0.015 for performance def 0.03 test
r.shadow.csm.maxcascades=2; 2,4,10 for performance
r.shadow.csm.transitionscale=1; 1,2 def 1 test
r.shadow.distancescale=0.8; 0.8,1,2 for performance def 1
r.shadow.filtermethod=0; def 0
r.shadow.forcesinglesampleshadowingfromstationary=0; def 0
r.shadow.loddistancefactor=8; 1,4,8 def 1 test
r.shadow.nanitelodbias=0; 2,1,0 for performance test
r.shadow.preshadowresolutionfactor=0.5; 0.5,1 for performance def 1
r.shadow.radiusthreshold=0.02; 0.06,0.05,0.04,0.03,0.02,0.01 for performance def 0.01
r.shadowquality=3; 3,4,5 for performance
r.viewdistancescale=0.8; 0.8,1 for performance def 1

;optional tests (add under base config)
r.aomaxviewdistance=10000; 10000,20000 is 100m,200m def 20000 test
r.distancefields.brickatlasmaxsizez=16; def 32 test
r.distancefields.maxpermeshresolution=128; def 256 test
r.lumenscene.globalsdf.clipmapextent=1000; def 2500 test
r.volumetriccloud.shadowmap.lightdistanceoverride=0; def 0
r.volumetricfog.distanceoverride=10000; 10000,12000 is 100m,120m def -1 test

;optional test (add under base config)
health.loghealthsnapshot=0; def 1 test
r.aoapplytostaticindirect=0; def 0 test
r.aoglobaldistancefield=1; def 1
r.aospecularocclusionmode=1; def 1 test
r.compileshadersfordevelopment=0; def 1
r.detectandwarnofbaddrivers=0;
r.gbufferdiffusesampleocclusion=0; def 0
r.gpucrash.collectionenable=0;
r.materiallogerroronfailure=0;
r.rhicmdbypass=0; def 0
r.sceneculling.explicitcellbounds=1; def 1
r.shadercompiler.jobcacheddc=1; def 1 test
r.shaders.removedeadcode=1; def 1
r.shaders.removeunusedinterpolators=1; def 0 test

;quality customize test (add under base config)
;r.dynamicglobalilluminationmethod=1; 0,1,2 none,lumen,ssgi
;r.reflectionmethod=1; 0,1,2 none,lumen,ssr
r.allowlandscapeshadows=1; 0 for performance
r.capsuleshadows=0; def 1 test
r.capsuleshadowsfullresolution=0; def 0
r.contactshadows.overrideshadowcastingintensity=50; def -1 test
r.contactshadows.standalone.method=0; def 0
r.contactshadows=1; def 1
r.dfshadowquality=2; 0,1,2,3 for performance def 3 test
r.distancefieldao=0; def 1 test
r.distancefieldshadowing=1; def 1
r.landscapelodbias=0; 1 for performance
r.lumen.diffuseindirect.allow=1; def 1 test
r.lumen.diffuseindirect.ssao=0; def 0 test
r.lumen.reflections.allow=1; def 1
r.lumen.reflections.maxroughnesstotrace=0.3; 0.1 for performance def -1 test
r.lumen.reflections.maxroughnesstotraceclamp=0.3; 0.1 for performance def 1 test
r.lumen.reflections.maxroughnesstotraceforfoliage=0; 0 for performance def 0.4 test
r.lumen.reflections.radiancecache=1; def 0 test
r.lumen.reflections.tracemeshsdfs=0; 0 for performance def 1 test
r.lumen.screenprobegather.radiancecache=1; def 1
r.lumen.screenprobegather.screenspacebentnormal=1; def 1
r.lumen.screenprobegather.shortrangeao.bentnormal=1; def 1
r.lumen.screenprobegather.shortrangeao=1; def 1 test
r.lumen.screenprobegather.tracemeshsdfs=0; 0 for performance def 1
r.lumen.tracemeshsdfs.allow=0; 0 for performance def 1
r.lumen.tracemeshsdfs=0; 0 for performance def 0 test
r.lumen.translucencyreflections.frontlayer.allow=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enableforproject=0; 0 for performance
r.lumen.translucencyreflections.radiancecache=1; def 1
r.lumen.translucencyvolume.radiancecache=1; def 1
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0; 0 for performance def 1 test
r.shadow.virtual.enable=1; def 1
r.shadow.virtual.forceonlyvirtualshadowmaps=1; def 1
r.shadow.virtual.resolutionlodbiaslocal=2; def 0 test
r.shadow.virtual.resolutionlodbiaslocalmoving=2; def 1 test
r.shadow.virtual.smrt.samplesperraydirectional=1; def 4 test
r.shadow.virtual.smrt.samplesperrayhair=1; def 1
r.shadow.virtual.smrt.samplesperraylocal=1; def 4 test
r.water.singlelayer.reflection=3; 0,2,3,1 def 1 test

;quality customize (add under base config)
fx.niagara.collision.cpuenabled=1; def 1 test
fx.niagara.qualitylevel=-1; 0,1,2,3 for performance def 3
r.allowhdr=0;
r.anisotropicmaterials=0; 0,1 for performance
r.aoquality=1; 0,1,2 for performance def 2
r.bloomquality=4;
r.decal.fadedurationscale=1; def 1 test
r.decal.fadescreensizemult=1; def 1
r.decal.stencilsizethreshold=0.1; def 0.1
r.defaultbackbufferpixelformat=4; def 4 test
r.depthoffieldquality=1; 0,1,2,3,4 for performance def 2
r.detailmode=2; 0,1,2,3 for performance def 3
r.dffullresolution=0; 0,1 def 0
r.dof.gather.accumulatorquality=0; 0,1 def 1
r.dof.gather.enablebokehsettings=0; 0,1 def 1
r.dof.kernel.maxbackgroundradius=0.012; 0.012,0.025 def 0.025
r.dof.kernel.maxforegroundradius=0.012; 0.012,0.025 def 0.025
r.dof.recombine.enablebokehsettings=0; 0,1 def 1
r.dof.recombine.quality=0; 0,1,2 def 2
r.dof.scatter.backgroundcompositing=1; 0,1,2 def 2
r.dof.scatter.enablebokehsettings=0; 0,1 def 1
r.dof.scatter.maxspriteratio=0.04; 0.04,0.1,0.25 def 0.1
r.emitter.fastpoolmaxfreesize=2097152; 2097152,4194304 def 2097152 test
r.emitterspawnratescale=0.5; 0.125,0.25,0.5,1 for performance
r.filmgrain=0; def 1
r.forwardshading.forceskylightcubemapblending=0; def 0
r.hairstrands.skyao=0; 0,1 def 1 test
r.hdr.enablehdroutput=0;
r.irisnormal=0; def 0 test
r.lensflarequality=2; 0,1,2
r.lightfunctionatlas.format=1; 0 for performance def 0 test
r.lightfunctionquality=1; 1,2,3 for performance def 2 test
r.lightshaftquality=1; 0,1 def 1
r.lumen.reflections.hiressurface=0; 0 for performance def 1
r.lumen.screenprobegather.downsamplefactor=32; 32,16 for performance def 16
r.lumen.screenprobegather.integratedownsamplefactor=1; 2,1 for performance def 1 test
r.lumen.screenprobegather.materialao=1; def 1 test
r.lumen.screenprobegather.radiancecache.proberesolution=8; 8,16,32 for performance def 32
r.lumen.screenprobegather.screentraces=0; 0 for performance def 1 test
r.lumen.screentracingsource=0; def 0 test
r.lumen.translucencyvolume.enable=1; def 1
r.lumenscene.radiosity=1; 0 for performance def 1
r.materialqualitylevel=1; 0,2,1,3 for performance def 1
r.maxanisotropy=16; 0,4,8 for performance
r.particlelightquality=1; 0,1,2 for performance def 2
r.postprocessing.downsamplequality=0; def 0 test
r.refraction.offsetquality=1; def 1
r.refractionquality=1; 0,1,2,3 for performance def 2 test
r.scenecolorformat=3; 2,3,4 for performance def 4
r.scenecolorfringe.max=0; def -1
r.scenecolorfringequality=0; 0,1
r.ssgi.enable=0; def 0
r.ssgi.quality=0; 0,2,3 for performance
r.ssr.halfresscenecolor=0; 1 for performance def 0 test
r.ssr.quality=2; 0,2,3 for performance def 3
r.sss.quality=-1; 0,-1,1 for performance def 0
r.subsurfacescattering=1; 0 for performance
r.tessellationadaptivepixelspertriangle=48; 999999,48 for performance
r.tonemapper.quality=5; 0,2,5
r.tonemapper.sharpen=2; 0,0.5,1,2 def -1
r.upscale.quality=2; 0,1,2,3,4 def 3
r.vrs.enable=0; def 0 test
r.vrs.enableimage=0; def 0 test
r.vrs.enablesoftware=1; def 0 test
r.vt.maxanisotropy=4; 2,4,8 for performance def 8
r.vt.splitphysicalpoolsize=64; 64 def 0 test
r.water.singlelayer.refractiondownsamplefactor=1; 2,1 for performance def 1
r.water.singlelayer.ssr=1; 0,1 for performance

;optional volumetrics customize test (add under base config)
r.fog=1; def 1
r.heterogeneousvolumes.downsamplefactor=2; 8,4,2,1 for performance def 1 test
r.heterogeneousvolumes.maxstepcount=256; 128,256,512 for performance def 512 test
r.heterogeneousvolumes.shadows.resolution=256; 128,256,512 for performance def 512 test
r.localfogvolume=0; 0 for performance def 1 test
r.skyatmosphere.samplelightshadowmap=0; 0 for performance skyatmosphere shadowing def 1
r.translucencylightingvolumedim=48; 32,48,64 for performance def 64
r.translucentlightingvolume=1; 0 for performance def 1
r.volumetriccloud.distancetosamplemaxcount=23; 30,25,23,20 def 15 test
r.volumetriccloud.enableatmosphericlightssampling=1; def 1
r.volumetriccloud.enabledistantskylightsampling=1; def 1
r.volumetriccloud.enablelocallightssampling=0; 0 for performance 1 is experimental def 0
r.volumetriccloud.reflectionraysamplemaxcount=20; 2,10,20,40 def 80 test
r.volumetriccloud.shadow.reflectionraysamplemaxcount=6; 2,4,6,12 def 24 test
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 0 for performance cloud shadowing def 1
r.volumetriccloud.shadow.viewraysamplemaxcount=6; 2,4,6,8 def 80 test
r.volumetriccloud.shadowmap.lightdistanceoverride=0; def 0
r.volumetriccloud.shadowmap.maxresolution=64; 64,128 def 2048 test
r.volumetriccloud.shadowmap.raysamplemaxcount=10; 10,12 def 128 test
r.volumetriccloud.shadowmap.spatialfiltering=1; 0,1,2,3,4 def 1
r.volumetriccloud.shadowmap=0; 0 for performance def 1 test
r.volumetriccloud.skyao=0; def 1
r.volumetriccloud.stepsizeonzeroconservativedensity=2; 4,2 def 1 test
r.volumetriccloud.viewraysamplemaxcount=256; 128,256,768 def 768 test
r.volumetriccloud=1; 0,1 for performance
r.volumetricfog.conservativedepth=1; 1 is experimental def 0 test
r.volumetricfog.depthdistributionscale=32; 16,32 def 32 test
r.volumetricfog.distanceoverride=-1; def -1 test
r.volumetricfog.emissive=1; 0 for performance def 1 test
r.volumetricfog.historymisssupersamplecount=2; 2,4,8 for performance test
r.volumetricfog.historyweight=0.95; 0.9,0.95,0.98 test
r.volumetricfog.injectshadowedlightsseparately=1; def 1 test
r.volumetricfog.lightfunction=1; def 1 test
r.volumetricfog.lightsoftfading=0; def 1 test
r.volumetricfog.upsamplejittermultiplier=0; 0 for performance
r.volumetricfog.useslightfunctionatlas=1; def 1
r.volumetricfog=1; 0,1 for performance
r.water.singlelayer.underwaterfogwhencameraisabovewater=0; def 0

;motionblur customize (add under base config)
r.blurgbuffer=0; 0,-1 def -1 test
r.defaultfeature.motionblur=0; def 1 test
r.fastblurthreshold=100; 0,3,7,16,100 def 7 test
r.motionblur.allowexternalvelocityflatten=1; def 1
r.motionblur.amount=-1; def -1 test
r.motionblur.halfresgather=0; 1,0 def 0
r.motionblur.halfresinput=1; def 1
r.motionblur.max=-1; def -1 test
r.motionblur.scale=1; def 1 test
r.motionblur.targetfps=-1; def -1
r.motionblur2ndscale=1; def 1
r.motionblurquality=0; 0,1,2,3,4 def 3 test
r.motionblurscatter=1; 0,1 def 0 test
r.motionblurseparable=1; 0,1 def 0 test

;ray tracing stuff (add under base config)
r.lumen.hardwareraytracing=0; def 0
r.lumen.radiancecache.hardwareraytracing=0; def 1 test
r.lumen.reflections.hardwareraytracing.translucent.refraction.enableforproject=0; def 1 test
r.lumen.reflections.hardwareraytracing=0; def 1 test
r.lumen.screenprobegather.hardwareraytracing=0; def 1 test
r.lumen.translucencyvolume.hardwareraytracing=0; def 1 test
r.lumenscene.directlighting.hardwareraytracing=0; def 1 test
r.lumenscene.farfield=0; def 0
r.lumenscene.radiosity.hardwareraytracing=0; def 1 test
r.manylights.hardwareraytracing=0; def 1 test
r.pathtracing=1; def 1
r.raytracing.enable=0; 0 disables lumen hardwareraytracing
r.raytracing.enableingame=0; 0 disables lumen hardwareraytracing
r.raytracing.enableondemand=0; def 0
r.raytracing.forceallraytracingeffects=0; def -1
r.raytracing.scene.buildmode=0; def 1
r.raytracing=0; 0 disables lumen hardwareraytracing

;optional psoprecache test (add under base config)
d3d12.pso.keepusedpsosinlowlevelcache=1; def 0 test
d3d12.psoprecache.keeplowlevel=1; def 0 test
fx.niagara.emitter.computepsoprecachemode=1; def 0 test
r.pso.precompilethreadpoolthreadpriority=2; def 2 test
r.psoprecache.globalshaders=1; def 1 test
r.psoprecache.proxycreationdelaystrategy=0; def 0
r.psoprecache.proxycreationwhenpsoready=1; def 1
r.psoprecaching=1; def 1
r.skipdrawonpsoprecaching=0; def 0
```

---

#### base config (add first)

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

[shadercompiler]
r.shaders.extradata=0; def 0

[systemsettings]
dp.allowscalabilitygroupstochangeatruntime=0; def 0

[texturestreaming]
poolsizevrampercentage=70; 50 to lower vram usage

[consolevariables]
d3d12.adjusttexturepoolsizebasedonbudget=0; 1 is experimental def 0 test
d3d12.syncwithdwm=0; def 0
fx.allowgpusorting=1; def 1
fx.batchasyncbatchsize=32; 16,32,64 test
fx.niagara.forcelasttickgroup=0; def 0 test
fx.niagaraallowgpuparticles=1; def 1
fx.niagaraallowruntimescalabilitychanges=1;
fx.qualitylevelspawnratescalereferencelevel=2; def 2
r.ambientocclusion.compute.smooth=1; def 1
r.ambientocclusion.compute=0; 0,1,2,3 def 0 test
r.ambientocclusion.method=0; 0,1 ssao or gtao def 0
r.ambientocclusionlevels=-1; 0,1,2,3 for performance def -1
r.ambientocclusionstaticfraction=-1; 0,1 for performance def -1
r.aoglobaldistancefield.mipfactor=4; 8,4 for performance def 4
r.bloom.screenpercentage=50; 50,100 def 50
r.chaos.reflectioncapturestaticsceneonly=1; def 1
r.d3d.forcedxc=0; multigpu def 0
r.d3d11.depth24bit=0; 1 for performance
r.d3d12.depth24bit=0; 1 for performance
r.d3d12.gpucrashdebuggingmode=0;
r.d3d12.shadowdepth32bit=0; 0 for performance
r.diffuseindirect.halfres=1; def 1
r.disabledistortion=0; def 0
r.dof.gather.postfiltermethod=1; 0,1,2 def 1
r.dof.gather.resolutiondivisor=2; 2,1 def 2
r.dof.gather.ringcount=4; 3,4,5 def 4
r.dof.scatter.foregroundcompositing=1; 0,1 def 1
r.dof.taa.cocbilateralfilterstrength=0; def 0 test
r.emitter.fastpoolenable=1; def 0
r.filter.loopmode=0; def 0 test
r.filter.sizescale=1; def 1
r.gtao.numangles=2; 2,4 def 2
r.hairstrands.composeaftertranslucency=1; def 1
r.hairstrands.deepshadow.supersampling=0; def 0
r.hairstrands.dofdepth=0; def 1 test
r.hairstrands.interpolation.usesingleguide=1; 1,0 for performance def 1
r.hairstrands.rasterizationscale=0.5; def 0.5
r.hairstrands.scatterscenelighting=1; def 1 test
r.hairstrands.shadow.castshadowwhennonvisible=1; def 1 test
r.hairstrands.skyao.samplecount=4; 2,4 def 4 test
r.hairstrands.skylighting.integrationtype=2; def 2
r.hairstrands.skylighting.samplecount=16; def 16
r.hairstrands.skylighting.screentraceocclusion=0; 0 for performance def 0
r.hairstrands.usecardsinsteadofstrands=0; 1 for performance def 0
r.hairstrands.velocityrasterizationscale=1; def 1.5 test
r.hairstrands.visibility.msaa.sampleperpixel=1; 1,2,4 for performance def 4
r.hairstrands.visibility.ppll=0; def 0
r.hairstrands.voxelization.virtual.voxelworldsize=0.3; def 0.3
r.lumen.irradiancefieldgather=0; 1 is experimental def 0
r.lumen.reflections.bilateralfilter=0; def 1
r.lumen.reflections.distantscreentraces=0; 0 for performance def 1 test
r.lumen.reflections.downsamplefactor=1; 2,1 for performance def 1 test
r.lumen.reflections.hairstrands.screentrace=0; def 1 test
r.lumen.reflections.hairstrands.voxeltrace=0; def 1 test
r.lumen.reflections.hierarchicalscreentraces.maxiterations=50; def 50
r.lumen.reflections.hierarchicalscreentraces.minimumoccupancy=0; def 0
r.lumen.reflections.maxbounces=0; 0,1,2 to 8 to 64 for performance def 0 test
r.lumen.reflections.roughnessfadelength=0.1; def 0.1
r.lumen.reflections.samplescenecolorathit=1; 0,1,2 for performance def 1 test
r.lumen.reflections.screenspacereconstruction.minweight=1; def 0 test
r.lumen.reflections.screenspacereconstruction.tonemapmode=2; def 1 test
r.lumen.reflections.screenspacereconstruction.tonemapstrength=1; def 0 test
r.lumen.reflections.screenspacereconstruction=1; def 1 test
r.lumen.reflections.screentraces=1; def 1 test
r.lumen.reflections.smoothbias=0; 0 for performance def 0 test
r.lumen.reflections.specularscale=1; test
r.lumen.screenprobegather.adaptiveprobeallocationfraction=0.4; 0.2,0.3,0.4 def 0.5 test
r.lumen.screenprobegather.extraambientocclusion=0; def 0 test
r.lumen.screenprobegather.fullresolutionjitterwidth=1; def 1
r.lumen.screenprobegather.hairstrands.screentrace=0; def 0 test
r.lumen.screenprobegather.hairstrands.voxeltrace=1; def 1 test
r.lumen.screenprobegather.importancesample=1; 0 for performance def 1 test
r.lumen.screenprobegather.irradianceformat=1; 1,0 for performance def 0 test
r.lumen.screenprobegather.numadaptiveprobes=8; 16,8 def 8 test
r.lumen.screenprobegather.radiancecache.gridresolution=48; 24,48 def 48
r.lumen.screenprobegather.radiancecache.numprobestotracebudget=200; 100,150,200,300 def 300 test
r.lumen.screenprobegather.screentraces.hzbtraversal.fullresdepth=0; 0,1 def 1 test
r.lumen.screenprobegather.shortrangeao.applyduringintegration=0; def 0 test
r.lumen.screenprobegather.shortrangeao.hairscreentrace=0; def 0 test
r.lumen.screenprobegather.shortrangeao.hairvoxeltrace=1; def 1 test
r.lumen.screenprobegather.stochasticinterpolation=1; 1,0 for performance def 0 test
r.lumen.screenprobegather.tracingoctahedronresolution=8; 8,16 def 8 test
r.lumen.screenprobegather.twosidedfoliagebackfacediffuse=1; 0,1 for performance def 1 test
r.lumen.translucencyvolume.enddistancefromcamera=2000; 500,1000,2000,3000 def 8000 test
r.lumen.translucencyvolume.gridpixelsize=64; 128,64,32 for performance def 32 test
r.lumen.translucencyvolume.radiancecache.gridresolution=12; 12,24 for performance def 24 test
r.lumen.translucencyvolume.radiancecache.nummipmaps=1; def 3 test
r.lumen.translucencyvolume.radiancecache.numprobestotracebudget=200; 100,125,150,175,200 def 200 test
r.lumen.translucencyvolume.radiancecache.probeatlasresolutioninprobes=128; def 128
r.lumen.translucencyvolume.radiancecache.proberesolution=8; def 8
r.lumen.translucencyvolume.spatialfilter.mode=1; def 1
r.lumen.translucencyvolume.spatialfilter.numpasses=2; def 2
r.lumen.translucencyvolume.spatialfilter.samplecount=3; def 3
r.lumen.translucencyvolume.spatialfilter.standarddeviation=5; def 5
r.lumen.translucencyvolume.spatialfilter=1; 0,1,2 def 1 test
r.lumen.translucencyvolume.tracefromvolume=1; def 1 test
r.lumen.translucencyvolume.tracingoctahedronresolution=3; 1,2,3 def 3
r.lumenscene.directlighting.maxlightspertile=4; 2,4,8 def 8 test
r.lumenscene.directlighting.updatefactor=64; 128,64,32 def 32 test
r.lumenscene.radiosity.hemisphereproberesolution=3; 2,3,4 for performance def 4
r.lumenscene.radiosity.probespacing=8; 16,8,4 for performance def 4
r.lumenscene.radiosity.updatefactor=96; 128,96,64 def 64 test
r.lumenscene.surfacecache.atlassize=2048; def 4096 test
r.lumenscene.surfacecache.cardcapturerefreshfraction=0.0625; 0,0.03125,0.0625,0.125 def 0.125
r.lumenscene.surfacecache.cardmaxresolution=64; def 512 test
r.lumenscene.surfacecache.cardmaxtexeldensity=0.05; def 0.2 test
r.lumenscene.surfacecache.cardminresolution=1; def 4 test
r.lumenscene.surfacecache.cardtexeldensityscale=25; def 100 test
r.minroughnessoverride=0; def 0
r.nanite.allowskinnedmeshes=1; 0,1 def 1 test
r.nanite.computerasterization=1; 1 for performance def 1 test
r.nanite.decompressdepth=0; 1 for performance def 0 test
r.nanite.dicingrate=2; 4,2 for performance def 2 test
r.nanite.meshshaderrasterization=1; gpu dependent def 1 test
r.nanite.softwarevrs=1; def 1
r.nanite.streaming.reservedresources=1; 1 is experimental def 0 test
r.nanite.viewmeshlodbias.min=-2; def -2
r.nanite.viewmeshlodbias.offset=0; def 0
r.postprocessing.downsamplechainquality=1; 0,1 def 1 test
r.postprocessing.prefercompute=0; gpu dependent def 0 test
r.postprocessing.quarterresolutiondownsample=0; 1 for performance def 0
r.postprocessingcolorformat=0; def 0
r.reflectioncapturesupersamplefactor=1; 1 for performance
r.reflectionenvironment=1; def 1
r.rendertargetpoolmin=400; 200,400,1000 to lower vram usage
r.shadow.denoiser=2; def 2
r.shadow.unbuiltpreviewingame=0; def 1
r.shadow.virtual.cache.forceinvalidatedirectional=0; def 0
r.shadow.virtual.distantlightforcecachefootprintfraction=0; 1,0.5,0 def 0 test
r.shadow.virtual.markpixelpagesmipmodelocal=1; 2,1,0 for performance def 0 test
r.shadow.virtual.nonnanite.includeincoarsepages=0; 0 performance def 1
r.shadow.virtual.nonnanite.usehzb=2; def 2
r.shadow.virtual.onepassprojection.maxlightsperpixel=8; 4,8,16,32 for performance def 16 test
r.shadow.virtual.onepassprojection=1; 1 for performance def 1
r.shadow.virtual.translucentquality=0; 0 for performance test
r.shadow.virtual.usefarshadowculling=1; def 1 test
r.shadow.virtual.usehzb=2; def 2
r.skyatmosphere.aerialperspectivelut.depthresolution=8; def 16 test
r.skyatmosphere.aerialperspectivelut.fastapplyonopaque=1; def 1
r.skyatmosphere.aerialperspectivelut.samplecountmaxperslice=1; def 4 test
r.skyatmosphere.aerialperspectivelut.width=8; def 32 test
r.skyatmosphere.fastskylut.samplecountmax=16; 16,32,64 for performance def 128
r.skyatmosphere.fastskylut.samplecountmin=2; 1,2,4 for performance def 4
r.skyatmosphere.lut32=0; 0 for performance def 0
r.skyatmosphere.multiscatteringlut.highquality=0; 0 for performance def 0
r.skyatmosphere.multiscatteringlut.samplecount=15; def 15
r.skyatmosphere.samplecountmax=16; 16,32,64 for performance def 128
r.skyatmosphere.samplecountmin=2; 1,2,4 for performance def 4
r.skyatmosphere.transmittancelut.samplecount=10; def 10
r.skyatmosphere.transmittancelut.usesmallformat=1; 1 for performance def 0
r.splinemesh.norecreateproxy=1; def 1
r.ssr.compute=1; def 0 test
r.ssr.maxroughness=0.95; 0.95,1 def -1 test
r.ssr.tiledcomposite=0; def 0
r.sss.burley.bilateralfilterkernelfunctiontype=1; 1,0 for performance
r.sss.burley.quality=1; 0,1 for performance
r.sss.checkerboard=2; 1,2,0 for performance
r.sss.halfres=1; 1,0 for performance
r.sss.sampleset=1; 0,1,2 for performance
r.sss.scale=1; 0,0.75,1 def 1
r.streaming.additionaltexturepoolsize=0; def 0
r.streaming.allowparallelrenderassetstreamingmanagerincrementalupdate=1; def 1
r.streaming.amortizecputogpucopy=0; def 0
r.streaming.boost=1; def 1
r.streaming.dropmips=0; 1 to lower vram usage
r.streaming.fullyloadmeshes=0;
r.streaming.fullyloadusedtextures=0;
r.streaming.hiddenprimitivescale=0.5; 0,0.25,0.5 for performance
r.streaming.limitpoolsizetovram=0; 0 to manually set poolsize
r.streaming.maxeffectivescreensize=0; def 0
r.streaming.maxnumtexturestostreamperframe=0; def 0
r.streaming.maxtempmemoryallowed=50; 50,75,100 to lower ram usage
r.streaming.maxtextureuvdensity=8; def 0 test
r.streaming.mipbias=0; 1 for performance def 0
r.streaming.poolsize.vrampercentageclamp=1024;
r.streaming.poolsizeformeshes=-1;
r.streaming.useallmips=0;
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=1; def 1 test
r.tonemapper.mergewithupscale.mode=0; def 0
r.translucency.autobeforedof=0.5; 0,0.5,1 def 0.5 test
r.virtualtexturereducedmemory=1; 1 to lower vram usage
r.volumetricrendertarget.reprojectionboxconstraint=0; def 0 test
r.vrs.basepass=2; def 2
r.vrs.contrastadaptiveshading=1; def 0 test
r.vrs.decals=2; def 2
r.vrs.lightfunctions=1; def 1
r.vrs.naniteemitgbuffer=2; def 2
r.vrs.reflectionenvironmentsky=2; def 2
r.vrs.ssao=0; def 0
r.vrs.ssr=2; def 2
r.vrs.translucency=1; def 1
r.vt.anisotropicfiltering=1; 0 for performance
r.vt.numgathertasks=2; 1,2,4,8 cpu dependent test
r.vt.poolsizescale=1; 0.8,1,2,4,8 to lower vram usage
r.water.enableshallowwatersimulation=0; 0 for performance test
r.water.enableunderwaterpostprocess=1; 0,1 for performance test
r.water.singlelayer.depthprepass=1; def 1
r.water.singlelayer.distancefieldshadow=0; def 1 test
r.water.singlelayer.tiledcomposite=1; def 1
r.water.singlelayer.vsmfiltering=0; def 0
```

---

#### optional async test skip unless you are testing
```python
;lumen async
r.lumen.asynccompute=1; def 1 test
r.lumen.diffuseindirect.asynccompute=1; def 1 test
r.lumen.reflections.asynccompute=1; def 0 test
r.lumenscene.lighting.asynccompute=1; def 1 test

;default test
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

;non default test
r.dfshadowasynccompute=1; def 0 test
r.enableasynccomputetranslucencylightingvolumeclear=1; def 0 test
r.megalights.asynccompute.generatesamples=1; def 0 test
r.megalights.asynccompute.volume=1; def 0 test
r.raytracing.asyncbuild=1; def 0 test
r.scenedepthhzbasynccompute=1; def 0 test
r.skyatmosphereasynccompute=1; def 0 test

;non default test (caution)
fx.batchasync=1; def 0 test
grass.grassmap.useasyncfetch=1; def 0 test
r.nanite.asyncrasterization.shadowdepths=1; def 0 test
r.postprocessing.forceasyncdispatch=1; def 0 test
r.shadow.shadowmapsrenderearly=1; def 0 test
r.volumetricrendertarget.preferasynccompute=1; def 0 test
```

---

#### open/create Input.ini and copy pasta %localappdata% (make read only unless it exist with code in it)

```python
[/script/engine.inputsettings]
baltentertogglesfullscreen=1;
benablemousesmoothing=0;
bf11togglesfullscreen=0;
bviewaccelerationenabled=0;

optional
buttonrepeatdelay=0.1;
doubleclicktime=0.01; def 0.1 test
initialbuttonrepeatdelay=0.1; def 0.2 test
```

---

#### ect

```python
upscaling to use
2560x1440 use 58%,67%,70%,77% for performance (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3328x1872 use 50%,58%,67%,70%,77% for performance (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3840x2160 use 33%,50%,58%,67%,70%,77% for performance (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

repak.bat method
zzz_inimods\engine\config\windows\windowsengine.ini
zzz_inimods\engine\config\windows\windowsinput.ini
```

---
