## updated 9/24/2026 ✂ 📋 🌀 :ramen: v1.5.9

#### quality ue4/5 config and for reference/customization/optimization/learning

#### open/create Engine.ini and copy pasta %localappdata% (make read only*)

#### check/change "for performance" options (left to right, performance to quality)

#### after pasta open game and change graphics to your spec then restart game*

#### recommended* to delete %localappdata%\nvidia\dxcache and %localappdata%\d3dscache

---

#### vram poolsize customize (add under base config)
```python
r.streaming.poolsize=2000; 400,600,800,1000,2000,3000,4000 to lower vram usage
```
#### match perfindexvalues_resolutionquality=/r.ngx.dlss.quality=/sg.resolutionquality= customize (add under base config)
```python
perfindexvalues_resolutionquality="50 50 50 50 50"; 33,50,59,67,77,100
r.mipmaplodbias=-1; -2.5,-2,-1.8,-1.6,-1.5,-1.4,-1,-0.5,0
r.ngx.dlss.quality=-1; -2,-1,0,1,2 ultra performance,performance,balanced,quality,ultra quality
sg.resolutionquality=50; 33,50,59,67,77,100
```
#### customize (add under base config)
```python
r.antialiasingmethod=4; 0,1,2,3,4 off,fxaa,taa,msaa,tsr def 4
r.defaultfeature.antialiasing=2; 0,1,2,3 off,fxaa,taa,msaa def 2
r.dof.temporalaaquality=1; def 1 test
r.fxaa.quality=3; 0,1,2,3,4,5 def 4
r.lumen.reflections.temporal=0; def 1 test
r.lumen.screenprobegather.temporal.distancethreshold=0.015; 0.015,0.005 def 0.005 test
r.lumen.screenprobegather.temporalfilterprobes=1; def 0 test
r.msaa.compositingsamplecount=1;
r.msaacount=0;
r.ngx.dlss.prefernissharpen=0; def 1
r.ngx.dlss.quality.auto=0; 0 for performance
r.ngx.dlss.reflections.temporalaa=0; def 1 test
r.ngx.dlss.sharpness=0; def 0
r.ngx.dlss.waterreflections.temporalaa=0; def 0 test
r.ngx.enableotherloggingsinks=0; def 0
r.ngx.loglevel=0; def 1
r.ngx.renamengxlogseverities=0; def 1
r.nis.enable=0;
r.nis.sharpness=0; def 0
r.nis.upscaling=0;
r.postprocessaaquality=6; 0 off 1,2 fxaa 3,4,5,6 taa
r.reflections.denoiser.temporalaccumulation=0; def 1 test
r.refraction.blur.temporalaa=0; def 1 test
r.refraction.blur=0; def 1 test
r.ssr.temporal=1; def 1
r.streamline.dlssg.checkstatusperframe=0; def 1 test
r.streamline.logfunctions=0;
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
t.streamline.reflex.auto=1; def 1
t.streamline.reflex.enable=1;
t.streamline.reflex.mode=2; 0,1,2
```
#### can cause crash in some games (add under base config)
```python
r.allowstaticlighting=0; def 1 test can cause crash
r.freeskeletalmeshbuffers=1; def 0 test can cause crash
r.hzbocclusion=1; scene depended test can cause crash
r.ngx.dlss.denoisermode=0; ray reconstruction test can cause crash
r.separatetranslucencyscreenpercentage=100; def 100 can cause crash
r.supportdepthonlyindexbuffers=0; def 1 test can cause crash
r.supportreversedindexbuffers=0; def 1 test can cause crash
```
#### latency customize (add under base config)
```python
d3d12.maximumframelatency=1; def 3 test
r.d3d11.useallowtearing=1; def 0
r.d3d12.useallowtearing=1; def 1
r.gtsynctype=0; 2 for vsync 1 for vrr 0 for lowest latency def 0
r.vsync=0; def 0
rhi.maximumframelatency=1; def 3 test
rhi.syncinterval=0; 1 for vsync 0 for lowest latency def 1
rhi.syncslackms=0; def 10
```
#### quality customize (add under base config)
```python
fx.niagara.collision.cpuenabled=1; def 1 test
fx.niagara.qualitylevel=2; 0,1,2,3 for performance def 3
r.allowhdr=0;
r.anisotropicmaterials=0; 0,1 for performance
r.aoquality=1; 0,1,2 for performance def 2
r.defaultbackbufferpixelformat=4; 0,4 8bit,10bit def 4 for hdr test
r.depthoffieldquality=1; 0,1,2,3,4 for performance def 2
r.detailmode=2; 0,1,2,3 for performance def 3
r.dffullresolution=0; 0,1 def 0
r.dfshadowquality=3; 0,1,2,3 for performance def 3 test
r.distancefieldao=1; 0 for performance
r.dof.gather.accumulatorquality=0; 0,1 def 1
r.dof.gather.enablebokehsettings=0; 0,1 def 1
r.dof.kernel.maxbackgroundradius=0.012; 0.012,0.025 def 0.025
r.dof.kernel.maxforegroundradius=0.012; 0.012,0.025 def 0.025
r.dof.recombine.enablebokehsettings=0; 0,1 def 1
r.dof.recombine.quality=0; 0,1,2 def 2
r.dof.scatter.backgroundcompositing=1; 0,1,2 def 2
r.dof.scatter.enablebokehsettings=0; 0,1 def 1
r.dof.scatter.maxspriteratio=0.04; 0.04,0.1,0.25 def 0.1
r.dynamicglobalilluminationmethod=1; 0 none 1 lumen 2 ssgi test
r.fog=1; def 1
r.hairstrands.skyao=0; 0,1 def 1 test
r.hdr.enablehdroutput=0;
r.heterogeneousvolumes.downsamplefactor=2; 8,4,2,1 for performance def 1 test
r.lensflarequality=2; 0,1,2
r.lightfunctionquality=1; 1,2,3 for performance def 2 test
r.lightshaftquality=1; 0,1 def 1
r.lumen.diffuseindirect.allow=1; def 1 test
r.lumen.diffuseindirect.ssao=0; def 0 test
r.lumen.reflections.allow=1; test
r.lumen.reflections.downsamplefactor=1; 2,1 for performance def 1 test
r.lumen.reflections.hiressurface=0; 0 for performance def 1
r.lumen.reflections.tracemeshsdfs=0; 0 for performance def 1 test
r.lumen.screenprobegather.downsamplefactor=32; 32,16 for performance def 16
r.lumen.screenprobegather.integratedownsamplefactor=1; 2,1 for performance def 1 test
r.lumen.screenprobegather.materialao=1; def 1 test
r.lumen.screenprobegather.radiancecache.proberesolution=16; 8,16,32 for performance def 32
r.lumen.screenprobegather.screenspacebentnormal=1; def 1 test
r.lumen.screenprobegather.screentraces=0; def 1 test
r.lumen.screenprobegather.shortrangeao.bentnormal=1; 0 for performance def 1 test
r.lumen.screenprobegather.shortrangeao=1; def 1 test
r.lumen.tracemeshsdfs.allow=0; 0,1 for performance def 1
r.lumen.tracemeshsdfs=0; 0 for performance def 0 test
r.lumen.translucencyreflections.frontlayer.allow=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0; 0 for performance
r.lumen.translucencyreflections.frontlayer.enableforproject=0; 0 for performance
r.lumen.translucencyvolume.enable=1; def 1
r.lumenscene.radiosity=1; 0,1 for performance def 1
r.materialqualitylevel=1; 0,2,1,3 for performance def 1
r.maxanisotropy=16; 0,4,8 for performance
r.particlelightquality=1; 0,1,2 for performance def 2
r.reflectionmethod=1; 0 none 1 lumen 2 ssr test
r.refractionquality=1; 0,1,2,3 for performance def 2 test
r.scenecolorformat=3; 2,3,4 for performance def 4
r.shadow.virtual.enable=1; 0 for performance def 1
r.shadow.virtual.forceonlyvirtualshadowmaps=1; def 1 test
r.skyatmosphere.samplelightshadowmap=0; 0 for performance volumetric shadows def 1
r.ssr.quality=2; 0,2,3 for performance def 3
r.sss.quality=-1; 0,-1,1 for performance def 0
r.supportmateriallayers=1; 0,1 for performance
r.tessellationadaptivepixelspertriangle=48; 999999,48 for performance
r.tonemapper.quality=5; 0,2,5
r.tonemapper.sharpen=1; 0,1,2
r.translucencylightingvolumedim=48; 32,48,64 for performance def 64
r.upscale.quality=2; 0,1,2,3,4 def 3
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0; 0 for performance volumetric shadows def 1
r.volumetriccloud.shadowmap=1; 0 for performance def 1 test
r.volumetriccloud=1; 0,1 for performance
r.volumetricfog.emissive=0; 0 for performance def 1
r.volumetricfog=1; 0,1 for performance
r.vrs.enable=1; def 0 test
r.vrs.enableimage=0; def 0
r.vrs.enablesoftware=1; def 0 test
r.vt.maxanisotropy=4; 2,4,8 for performance def 8
r.water.singlelayer.reflection=3; 0,2,3,1 def 1 test
r.water.singlelayer.refractiondownsamplefactor=1; 2,1 for performance def 1
r.water.singlelayer.ssr=1; 0,1 for performance
r.water.singlelayerwater.supportcloudshadow=1; def 0 test
```
#### motionblur customize (add under base config)
```python
r.blurgbuffer=0; 0,-1 def -1 test
r.defaultfeature.motionblur=0; def 1 test
r.fastblurthreshold=100; 0,3,7,16,100 def 7 test
r.motionblur.allowexternalvelocityflatten=1; def 1
r.motionblur.amount=-1; def -1 test
r.motionblur.halfresgather=0; 1,0 def 0
r.motionblur.halfresinput=1; def 1
r.motionblur.max=-1; def -1 test
r.motionblur.scale=0.3; def 1 test
r.motionblur.targetfps=-1; def -1
r.motionblur2ndscale=1; def 1
r.motionblurquality=0; 0,1,2,3,4 def 4 test
r.motionblurscatter=1; 0,1 def 0 test
r.motionblurseparable=1; 0,1 def 0 test
```
#### ray tracing disabled only lumen software in UE5 test (add under base config)
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
r.raytracing.raytracingproxies.projectenabled=0; test
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

[texturestreaming]
poolsizevrampercentage=70; 50 to lower vram usage

[consolevariables]
dp.allowscalabilitygroupstochangeatruntime=0; def 0
d3d12.adjusttexturepoolsizebasedonbudget=0; 1 is experimental test
d3d12.syncwithdwm=0; def 0
fx.allowgpusorting=1;
fx.batchasyncbatchsize=32; 16,32,64 test
fx.niagaraallowgpuparticles=1;
fx.niagaraallowruntimescalabilitychanges=1;
fx.qualitylevelspawnratescalereferencelevel=2; def 2
health.loghealthsnapshot=0; def 1 test
r.allowlandscapeshadows=1; 0 for performance
r.allowsubprimitivequeries=1; def 1
r.ambientocclusion.compute.smooth=1; def 1
r.ambientocclusion.compute=0; 0,1,2,3 def 0 test
r.ambientocclusion.method=0; 0,1 ssao or gtao def 0
r.ambientocclusionlevels=-1; 0,1,2,3 for performance def -1
r.ambientocclusionmaxquality=100; -60,100 test
r.ambientocclusionmiplevelfactor=0.4; 1,0.6,0.4 def 0.4 test
r.ambientocclusionradiusscale=1; 0.85,1 def 1
r.ambientocclusionstaticfraction=-1; 0,1 for performance def -1
r.aoapplytostaticindirect=0; def 0 test
r.aoglobaldistancefield.mipfactor=4; 8,4 for performance def 4
r.aoglobaldistancefield=1; def 1
r.aomaxviewdistance=10000; 10000,20000 is 100m,200m def 20000 test
r.aospecularocclusionmode=1; def 1 test
r.bloom.screenpercentage=50; 50,100 def 50
r.bloomquality=4;
r.capsuleshadows=0; 0,1 for performance
r.capsuleshadowsfullresolution=0; def 0
r.chaos.reflectioncapturestaticsceneonly=1; def 1
r.compileshadersfordevelopment=0; def 1
r.contactshadows.overrideshadowcastingintensity=50; def -1 test
r.contactshadows.standalone.method=0; def 0 test
r.contactshadows=1; 0,1 for performance
r.d3d.forcedxc=0; multigpu def 0
r.d3d11.depth24bit=0; 1 for performance
r.d3d12.depth24bit=0; 1 for performance
r.d3d12.gpucrashdebuggingmode=0;
r.d3d12.shadowdepth32bit=0; 0 for performance
r.decal.fadedurationscale=1; def 1 test
r.decal.fadescreensizemult=1; def 1
r.decal.stencilsizethreshold=0.1; def 0.1
r.detectandwarnofbaddrivers=0;
r.diffuseindirect.halfres=1; def 1
r.disabledistortion=0; test
r.disablelandscapenanitegi=1; def 1
r.distancefields.brickatlasmaxsizez=16; def 32 test
r.distancefields.maxpermeshresolution=128; 128,256 to lower vram usage
r.distancefieldshadowing=1; 0 for performance
r.dof.gather.postfiltermethod=1; 0,1,2 def 1
r.dof.gather.resolutiondivisor=2; 2,1 def 2
r.dof.gather.ringcount=4; 3,4,5 def 4
r.dof.scatter.foregroundcompositing=1; 0,1 def 1
r.dof.taa.cocbilateralfilterstrength=0; def 0 test
r.dynamicres.operationmode=0;
r.emitter.fastpoolenable=1;
r.emitter.fastpoolmaxfreesize=4194304; 2097152,4194304 test
r.emitterspawnratescale=0.5; 0.125,0.25,0.5,1 for performance
r.filmgrain=0;
r.filter.loopmode=0; def 0 test
r.filter.sizescale=1; def 1
r.finishcurrentframe=0; 1 for latency cost too much
r.forcedebugviewmodes=2; faster shader iteration
r.forwardshading.forceskylightcubemapblending=0; def 0
r.fullscreenmode=0; 0,1 fullscreen,windowed
r.gbufferdiffusesampleocclusion=0; def 0
r.gpucrash.collectionenable=0;
r.gtao.numangles=2; 2,4 def 2
r.hairstrands.composeaftertranslucency=1;
r.hairstrands.deepshadow.supersampling=0;
r.hairstrands.dofdepth=0; def 1 test
r.hairstrands.interpolation.usesingleguide=1; 1,0 for performance def 1
r.hairstrands.minlod=0;
r.hairstrands.rasterizationscale=0.5;
r.hairstrands.scatterscenelighting=1; def 1 test
r.hairstrands.shadow.castshadowwhennonvisible=1; def 1 test
r.hairstrands.skyao.samplecount=4; 2,4 def 4 test
r.hairstrands.skylighting.integrationtype=2; def 2
r.hairstrands.skylighting.jitterintegration=0; 0 for performance test
r.hairstrands.skylighting.screentraceocclusion=0; 0 for performance test
r.hairstrands.usecardsinsteadofstrands=0; 1 for performance
r.hairstrands.velocityrasterizationscale=0.5; 0.5,1,1.5 for performance
r.hairstrands.visibility.msaa.sampleperpixel=1; 1,2,4 for performance def 4
r.hairstrands.visibility.ppll=0; def 0
r.heterogeneousvolumes.maxstepcount=256; 128,256,512 for performance def 512 test
r.heterogeneousvolumes.shadows.resolution=256; 128,256,512 for performance def 512 test
r.irisnormal=0; def 0 test
r.landscapelodbias=0; 1 for performance
r.lightfunctionatlas.format=1; 0 for performance def 0 test
r.lumen.reflections.bilateralfilter=0; 0,1 for performance def 1
r.lumen.reflections.distantscreentraces=0; 0 for performance def 1 test
r.lumen.reflections.downsamplecheckerboard=0; def 0 test
r.lumen.reflections.hairstrands.screentrace=0; test
r.lumen.reflections.hairstrands.voxeltrace=0; test
r.lumen.reflections.hierarchicalscreentraces.maxiterations=50;
r.lumen.reflections.hierarchicalscreentraces.minimumoccupancy=0;
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
r.lumen.screenprobegather.adaptiveprobeallocationfraction=0.4; 0.2,0.3,0.4 def 0.5 test
r.lumen.screenprobegather.extraambientocclusion=0; def 0 test
r.lumen.screenprobegather.fullresolutionjitterwidth=1; 0.25 to 8 def 1 test
r.lumen.screenprobegather.importancesample=1; 0 for performance def 1 test
r.lumen.screenprobegather.irradianceformat=1; 1,0 for performance def 0 test
r.lumen.screenprobegather.numadaptiveprobes=16; 16,8 def 8 test
r.lumen.screenprobegather.radiancecache.numprobestotracebudget=100; 100,150,200,300 def 300 test
r.lumen.screenprobegather.screentraces.hzbtraversal.fullresdepth=1; 0,1 def 1 test
r.lumen.screenprobegather.shortrangeao.applyduringintegration=0; def 0 test
r.lumen.screenprobegather.shortrangeao.hairscreentrace=0; test
r.lumen.screenprobegather.shortrangeao.hairvoxeltrace=0; 0 for performance def 1 test
r.lumen.screenprobegather.stochasticinterpolation=1; 1,0 for performance def 0 test
r.lumen.screenprobegather.tracingoctahedronresolution=8; 8,16 def 8 test
r.lumen.screenprobegather.twosidedfoliagebackfacediffuse=0; 0,1 for performance def 1 test
r.lumen.translucencyvolume.enddistancefromcamera=2000; 500,1000,2000,3000 def 8000 test
r.lumen.translucencyvolume.gridpixelsize=64; 128,64,32 for performance def 32 test
r.lumen.translucencyvolume.radiancecache.gridresolution=24; 12,24 for performance def 24 test
r.lumen.translucencyvolume.radiancecache.nummipmaps=1; def 3 test
r.lumen.translucencyvolume.radiancecache.numprobestotracebudget=200; 100,125,150,175,200 def 200 test
r.lumen.translucencyvolume.radiancecache.probeatlasresolutioninprobes=128; def 128
r.lumen.translucencyvolume.radiancecache.proberesolution=8; def 8
r.lumen.translucencyvolume.radiancecache=1; 0 for performance def 1 test
r.lumen.translucencyvolume.spatialfilter.mode=1; def 1
r.lumen.translucencyvolume.spatialfilter.numpasses=2; def 2
r.lumen.translucencyvolume.spatialfilter.samplecount=3; def 3
r.lumen.translucencyvolume.spatialfilter.standarddeviation=5; def 5
r.lumen.translucencyvolume.spatialfilter=1; 0,1,2 def 1 test
r.lumen.translucencyvolume.tracefromvolume=0; 0 for performance def 1 test
r.lumen.translucencyvolume.tracingoctahedronresolution=3; 1,2,3 def 3
r.lumenscene.directlighting.maxlightspertile=4; 2,4,8 def 8 test
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0; 0 for performance def 1 test
r.lumenscene.directlighting.updatefactor=64; 128,64,32 def 32 test
r.lumenscene.globalsdf.notcoveredexpandsurfacescale=0.7; def 0.6 test
r.lumenscene.radiosity.hemisphereproberesolution=3; 2,3,4 for performance def 4
r.lumenscene.radiosity.probespacing=8; 16,8,4 for performance def 4
r.lumenscene.radiosity.updatefactor=128; 128,64 def 64 test
r.lumenscene.surfacecache.atlassize=2048; def 4096 test
r.lumenscene.surfacecache.cardcapturerefreshfraction=0.0625; 0,0.03125,0.0625,0.125 def 0.125
r.lumenscene.surfacecache.cardmaxresolution=64; def 512 test
r.lumenscene.surfacecache.cardmaxtexeldensity=0.05; def 0.2 test
r.lumenscene.surfacecache.cardminresolution=1; def 4 test
r.lumenscene.surfacecache.cardtexeldensityscale=25; def 100 test
r.materiallogerroronfailure=0;
r.minroughnessoverride=0; def 0
r.nanite.allowskinnedmeshes=1; 0,1 def 1 test
r.nanite.computerasterization=1; 1 for performance def 1 test
r.nanite.decompressdepth=0; 1 for performance def 0 test
r.nanite.dicingrate=2; 4,2 for performance def 2 test
r.nanite.meshshaderrasterization=1; def 1 test
r.nanite.softwarevrs=1; def 1
r.nanite.viewmeshlodbias.min=-2; def -2
r.nanite.viewmeshlodbias.offset=0; def 0
r.numbufferedocclusionqueries=1; test
r.oneframethreadlag=1; 0 for latency cost too much
r.postprocessing.prefercompute=0; gpu dependent def 0 test
r.postprocessing.quarterresolutiondownsample=0; 1 for performance def 0
r.reflectioncapturesupersamplefactor=1; 1 for performance
r.refraction.offsetquality=1; def 1
r.rendertargetpoolmin=400; 200,400,1000 to lower vram usage
r.rhicmdbypass=0; def 0
r.scenecolorfringe.max=0; def -1
r.scenecolorfringequality=0; 0,1
r.sceneculling.explicitcellbounds=0; 0 for performance
r.screenpercentage.default=100; def 100
r.screenpercentage.maxresolution=0; def 0
r.screenpercentage.minresolution=0; def 0
r.secondaryscreenpercentage.gameviewport=0; def 0
r.separatetranslucency=1; def 1
r.separatetranslucencyupsamplemode=1; def 1
r.shaders.removedeadcode=1; def 1
r.shaders.removeunusedinterpolators=0; def 0 test
r.shadow.unbuiltpreviewingame=0; def 1
r.shadow.virtual.cache.forceinvalidatedirectional=0; def 0
r.shadow.virtual.distantlightforcecachefootprintfraction=1; 1,0 def 0 test
r.shadow.virtual.markpixelpagesmipmodelocal=2; 2,1,0 for performance def 0 test
r.shadow.virtual.maxphysicalpages=1024; 512,1024,2048,4096 to lower vram usage test
r.shadow.virtual.nonnanite.includeincoarsepages=0; 0 performance def 1
r.shadow.virtual.nonnanite.usehzb=2; def 2
r.shadow.virtual.onepassprojection.maxlightsperpixel=8; 4,8,16,32 for performance
r.shadow.virtual.onepassprojection=1; 1 for performance def 1
r.shadow.virtual.pagemarkingpixelstridex=4; 6,4,2 def 2 test
r.shadow.virtual.pagemarkingpixelstridey=4; 6,4,2 def 2 test
r.shadow.virtual.resolutionlodbiasdirectional=-0.5; -0.5,-0.75,-1,-1.5 def -1.5 test
r.shadow.virtual.resolutionlodbiasdirectionalmoving=-0.5; -0.5,-0.75,-1,-1.5 def -1.5 test
r.shadow.virtual.resolutionlodbiaslocal=2; 3,2,1,0 for performance def 0 test
r.shadow.virtual.resolutionlodbiaslocalmoving=2; 3,2,1 for performance def 1 test
r.shadow.virtual.smrt.adaptiveraycount=1; def 1
r.shadow.virtual.smrt.extrapolatemaxslopelocal=0; 0 for performance def 0.05 test
r.shadow.virtual.smrt.raycountdirectional=3; 0,2,3,4,8 def 8 test
r.shadow.virtual.smrt.raycountlocal=2; 0,2,3,4,8 def 8 test
r.shadow.virtual.smrt.raylengthscaledirectional=0.4; def 1.5 test
r.shadow.virtual.smrt.samplesperraydirectional=2; 1,2,4 test
r.shadow.virtual.smrt.samplesperraylocal=2; 0,1,2,4 def 4 test
r.shadow.virtual.smrt.texelditherscaledirectional=2; def 2 test
r.shadow.virtual.smrt.texelditherscalelocal=6; 2,4,6 def 2 test
r.shadow.virtual.translucentquality=0; 0 for performance test
r.shadow.virtual.usefarshadowculling=1; def 1 test
r.shadow.virtual.usehzb=2; def 2
r.skyatmosphere.fastskylut.samplecountmax=32; 32,64 for performance
r.skyatmosphere.fastskylut.samplecountmin=1; 1,4 for performance
r.skyatmosphere.lut32=0; 0 for performance
r.skyatmosphere.multiscatteringlut.highquality=0; 0 for performance
r.skyatmosphere.multiscatteringlut.samplecount=15;
r.skyatmosphere.samplecountmax=32; 32,64 for performance
r.skyatmosphere.samplecountmin=1; 1,4 for performance
r.skyatmosphere.transmittancelut.samplecount=10;
r.skyatmosphere.transmittancelut.usesmallformat=0; 1 for performance
r.splinemesh.norecreateproxy=1; def 1
r.ssgi.enable=0; def 0
r.ssgi.quality=0; 0,2,3 for performance
r.ssr.compute=1; def 0 test
r.ssr.halfresscenecolor=1; 1,0 for performance
r.ssr.maxroughness=0.95; 0.95,1 def -1 test
r.ssr.tiledcomposite=0; def 0
r.sss.burley.bilateralfilterkernelfunctiontype=1; 1,0 for performance
r.sss.burley.quality=1; 0,1 for performance
r.sss.checkerboard=2; 1,2,0 for performance
r.sss.halfres.forceseparable=1; 1,0 for performance
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
r.streaming.maxtempmemoryallowed=100; 50,75,100 to lower ram usage
r.streaming.mipbias=0; 1 for performance def 0
r.streaming.poolsize.vrampercentageclamp=1024;
r.streaming.poolsizeformeshes=-1;
r.streaming.useallmips=0;
r.streaming.usefixedpoolsize=0;
r.streaming.usepertexturebias=1; def 1 test
r.subsurfacescattering=1; 0 for performance
r.supportallshaderpermutations=0; def 0
r.translucency.autobeforedof=0.5; 0,0.5,1 def 0.5 test
r.translucency.standardseparated=0; def 0
r.translucentlightingvolume=1; 0 for performance def 1
r.useparallelgetdynamicmeshelementstasks=0; def 0 test
r.usepreexposure=0; test
r.virtualtexturereducedmemory=1; 1 to lower vram usage
r.volumetriccloud.distancetosamplemaxcount=23; 30,25,23,20 def 15 test
r.volumetriccloud.enableatmosphericlightssampling=1; def 1
r.volumetriccloud.enabledistantskylightsampling=1; def 1
r.volumetriccloud.enablelocallightssampling=0; 0 for performance
r.volumetriccloud.reflectionraysamplemaxcount=20; 2,10,20,40 def 80 test
r.volumetriccloud.shadow.reflectionraysamplemaxcount=6; 2,4,6,12 def 24 test
r.volumetriccloud.shadow.viewraysamplemaxcount=6; 2,4,6,8 def 80 test
r.volumetriccloud.shadowmap.maxresolution=64; 64,128 def 2048 test
r.volumetriccloud.shadowmap.raysamplemaxcount=10; 10,12 def 128 test
r.volumetriccloud.shadowmap.spatialfiltering=1; 0,1,2,3,4 def 1
r.volumetriccloud.skyao=0; def 1
r.volumetriccloud.stepsizeonzeroconservativedensity=2; 4,2 def 1 test
r.volumetriccloud.support=1; def 1
r.volumetriccloud.viewraysamplemaxcount=256; 128,256,768 def 768 test
r.volumetricfog.conservativedepth=0;
r.volumetricfog.depthdistributionscale=32; 16,32 def 32 test
r.volumetricfog.historymisssupersamplecount=2; 2,4,8 for performance test
r.volumetricfog.historyweight=0.95; 0.9,0.95,0.98 test
r.volumetricfog.injectshadowedlightsseparately=1; def 1 test
r.volumetricfog.lightfunction=1; def 1 test
r.volumetricfog.lightsoftfading=1; def 1 test
r.volumetricfog.upsamplejittermultiplier=0; 0 for performance
r.volumetricfog.useslightfunctionatlas=1; def 1
r.vrs.basepass=2; def 2
r.vrs.contrastadaptiveshading=1; def 0
r.vrs.decals=2; def 2
r.vrs.lightfunctions=1; def 1
r.vrs.naniteemitgbuffer=2; def 2
r.vrs.reflectionenvironmentsky=2; def 2
r.vrs.ssao=0; def 0
r.vrs.ssr=2; def 2
r.vrs.support=1; def 1
r.vrs.translucency=1; def 1
r.vt.anisotropicfiltering=1; 0 for performance
r.vt.numgathertasks=1; 1,2,4,8 cpu dependent test
r.vt.poolsizescale=0.8; 0.8,1,2,4,8 to lower vram usage
r.water.enableshallowwatersimulation=0; 0 for performance test
r.water.enableunderwaterpostprocess=1; 0,1 for performance test
r.water.singlelayer.depthprepass=1; def 1
r.water.singlelayer.distancefieldshadow=0; def 1 test
r.water.singlelayer.rtr=0;
r.water.singlelayer.shaderssupportdistancefieldshadow=0; def 1 test
r.water.singlelayer.shaderssupportvsmfiltering=0; def 0
r.water.singlelayer.tiledcomposite=1; def 1
r.water.singlelayer.underwaterfogwhencameraisabovewater=0; def 0
r.water.singlelayer.vsmfiltering=0; def 0
r.water.singlelayer=1; def 1
t.maxfps=-1;
```

---

#### optional psoprecache test (add under base config)
```python
d3d12.pso.keepusedpsosinlowlevelcache=1; def 0 test
d3d12.psoprecache.keeplowlevel=1; def 0 test
fx.niagara.emitter.computepsoprecachemode=1; def 0 test
r.psoprecache.globalshaders=1; def 0 test
r.psoprecache.proxycreationdelaystrategy=0; def 0
r.psoprecache.proxycreationwhenpsoready=1; def 1
r.psoprecaching=1; def 1
r.skipdrawonpsoprecaching=0; def 0
```
#### optional async defaults test (add under base config)
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
#### optional async test skip unless you are testing
```python
r.dfshadowasynccompute=1; def 0 test
r.enableasynccomputetranslucencylightingvolumeclear=1; def 0 test
r.lumen.reflections.asynccompute=1; def 0 test
r.megalights.asynccompute.generatesamples=1; def 0 test
r.megalights.asynccompute.volume=1; def 0 test
r.raytracing.asyncbuild=1; def 0 test
r.scenedepthhzbasynccompute=1; def 0 test
r.skyatmosphereasynccompute=1; def 0 test

caution
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
