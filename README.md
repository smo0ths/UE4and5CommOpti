## updated 3/1/2025 ✂ 📋 🌀 :ramen: v1.0.2a [(twitch)](https://twitch.tv/smoothschannel) [(paypal support)](https://www.paypal.com/donate/?business=krtr5pj8dlata&no_recurring=0&item_name=dono&currency_code=usd) [(streamlabs support)](https://streamlabs.com/smoothschannel/tip)

### quality ue4/5 config and for reference/customization/optimization/learning

## open engine.ini and copy pasta %localappdata%

#### check 🔴 options for more fps (left to right, performance to quality, or remove)

#### after pasting ini start game and set graphic settings to your spec low/med/high/ultra then restart game*

```python
[core.log]
global=off ;

[crashreportclient]
ballowtobecontacted=0 ;
bisallowedtoclosewithoutsending=1 ;
bsendlogfile=0 ;
cansendwhenuifailedtoinitialize=0 ;
datarouterurl="" ;
uiinitretrycount=0 ;

[/script/engine.engine]
bpauseonlossoffocus=0 ;
bsmoothframerate=0 ;
busefixedframerate=0 ;

[texturestreaming]
poolsizevrampercentage=70 ; 🔴 50 to lower vram usage

[consolevariables]
d3d12.maximumframelatency=1 ;
d3d12.texturepoolonlyaccountstreamabletexture=1 ;
fx.gpusimulationtexturesizex=32 ;
fx.gpusimulationtexturesizey=32 ;
fx.niagara.asyncgputrace.globalsdfenabled=0 ;
fx.niagara.asyncgputrace.hwraytraceenabled=0 ;
fx.niagara.collision.cpuenabled=0 ;
fx.niagara.qualitylevel=3 ; 🔴 0,1,2 for performance
fx.niagaraallowruntimescalabilitychanges=1 ;
r.allowlandscapeshadows=1 ; 🔴 0 for performance
r.ambientocclusionlevels=-1 ; 🔴 0,1 for performance
r.ambientocclusionmaxquality=100 ;
r.ambientocclusionstaticfraction=-1 ; 🔴 0 for performance
r.anisotropicmaterials=1 ; 🔴 0 for performance
r.antialiasingmethod=4 ;
r.aoquality=2 ; 🔴 0 for performance
r.bloom.asynccompute=1 ;
r.bloom.screenpercentage=50 ;
r.bloomquality=4 ; 🔴 0 for performance
r.blurgbuffer=0 ;
r.capsuleshadows=0 ; 🔴 0 for performance
r.chaos.reflectioncapturestaticsceneonly=1 ;
r.contactshadows=1 ;
r.d3d.forcedxc=1 ;
r.d3d11.useallowtearing=1 ;
r.d3d12.allowasynccompute=1 ;
r.d3d12.allowshadermodel6=1 ;
r.d3d12.gpucrashdebuggingmode=0 ;
r.d3d12.shadowdepth32bit=0 ; 🔴 0 for performance
r.d3d12.useallowtearing=1 ;
r.depthoffieldquality=0 ; 🔴 0,1 for performance
r.detectandwarnofbaddrivers=0 ;
r.dffullresolution=0 ; 🔴 0 for performance
r.dfshadowasynccompute=1 ;
r.dfshadowquality=2 ; 🔴 1,2 for performance
r.distancefields.supportevenifhardwareraytracingsupported=0 ;
r.dof.gather.accumulatorquality=0 ;
r.dof.gather.enablebokehsettings=0 ;
r.dof.gather.postfiltermethod=1 ;
r.dof.gather.ringcount=3 ;
r.dof.kernel.maxbackgroundradius=0.012 ;
r.dof.kernel.maxforegroundradius=0.012 ;
r.dof.recombine.quality=0 ;
r.dof.scatter.backgroundcompositing=0 ;
r.dof.scatter.enablebokehsettings=0 ;
r.dof.scatter.foregroundcompositing=0 ;
r.dof.scatter.maxspriteratio=0.04 ;
r.dof.temporalaaquality=0 ;
r.dynamicres.operationmode=0 ;
r.emitterspawnratescale=1 ; 🔴 0.125,0.25,0.5 for performance
r.fidelityfx.fsr.enabled=0 ;
r.fidelityfx.fsr2.enabled=0 ;
r.fidelityfx.fsr3.enabled=0 ;
r.filmgrain=0 ;
r.filter.loopmode=0 ; 🔴 0 for performance
r.filter.sizescale=1 ;
r.fog=1 ;
r.fxaa.quality=4 ;
r.gpucrash.collectionenable=0 ;
r.gpuscene.parallelupdate=1 ;
r.gtsynctype=0 ;
r.hairstrands.composeaftertranslucency=0 ;
r.hairstrands.deepshadow.supersampling=0 ;
r.hairstrands.interpolation.usesingleguide=1 ; 🔴 1 for performance
r.hairstrands.minlod=0 ;
r.hairstrands.rasterizationscale=0.5 ;
r.hairstrands.scatterscenelighting=1 ;
r.hairstrands.shadow.castshadowwhennonvisible=0 ;
r.hairstrands.skyao=0 ; 🔴 0 for performance
r.hairstrands.skylighting.integrationtype=2 ;
r.hairstrands.skylighting.screentraceocclusion=0 ;
r.hairstrands.usecardsinsteadofstrands=0 ; 🔴 1 for performance
r.hairstrands.velocityrasterizationscale=1 ;
r.hairstrands.visibility.msaa.sampleperpixel=1 ; 🔴 1,2 for performance
r.hairstrands.visibility.ppll=0 ; 🔴 0 for performance
r.hairstrands.voxelization.voxelsizeinpixel=0.3 ;
r.hairstrands.voxelization=0 ; 🔴 0 for performance
r.heterogeneousvolumes.hardwareraytracing=0 ;
r.hzbocclusion=1 ;
r.landscapelodbias=0 ; 🔴 1 for performance
r.lightmaxdrawdistancescale=1 ; 🔴 0.6 for performance
r.lumen.asynccompute=1 ;
r.lumen.diffuseindirect.allow=1 ;
r.lumen.diffuseindirect.asynccompute=1 ;
r.lumen.hardwareraytracing.lightingmode=0 ;
r.lumen.hardwareraytracing=1 ; 🔴 0 for performance
r.lumen.radiancecache.hardwareraytracing.retrace.farfield=0 ;
r.lumen.radiancecache.hardwareraytracing=1 ;
r.lumen.reflections.allow=1 ;
r.lumen.reflections.asynccompute=1 ;
r.lumen.reflections.bilateralfilter.numsamples=4 ;
r.lumen.reflections.bilateralfilter.spatialkernelradius=0.002 ;
r.lumen.reflections.bilateralfilter=1 ;
r.lumen.reflections.distantscreentraces=1 ;
r.lumen.reflections.downsamplefactor=1 ; 🔴 2 for performance
r.lumen.reflections.hairstrands.screentrace=1 ;
r.lumen.reflections.hairstrands.voxeltrace=1 ;
r.lumen.reflections.hardwareraytracing.retrace.farfield=0 ;
r.lumen.reflections.hardwareraytracing=1 ;
r.lumen.reflections.maxroughnesstotrace=0.4 ; 🔴 -1,0.4 for performance
r.lumen.reflections.maxroughnesstotraceforfoliage=0.4 ;
r.lumen.reflections.samplescenecolorathit=1 ;
r.lumen.reflections.screenspacereconstruction=1 ;
r.lumen.reflections.screentraces=1 ;
r.lumen.reflections.smoothbias=0.4 ; 🔴 0,0.4 for performance
r.lumen.reflections.specularindirectbuffer32bit=1 ; 🔴 1 for performance
r.lumen.reflections.tracemeshsdfs=0 ; 🔴 0 for performance
r.lumen.screenprobegather.downsamplefactor=16 ; 🔴 16,32 for performance
r.lumen.screenprobegather.hardwareraytracing.retrace.farfield=0 ;
r.lumen.screenprobegather.hardwareraytracing=1 ;
r.lumen.screenprobegather.materialao=1 ;
r.lumen.screenprobegather.shortrangeao.hardwareraytracing=0 ;
r.lumen.screenprobegather.stochasticinterpolation=1 ; 🔴 1 for performance
r.lumen.tracemeshsdfs.allow=0 ; 🔴 0 for performance
r.lumen.tracemeshsdfs.tracedistance=180 ;
r.lumen.tracemeshsdfs=0 ; 🔴 0 for performance
r.lumen.translucencyreflections.frontlayer.allow=0 ; 🔴 0 for performance
r.lumen.translucencyreflections.frontlayer.enable=0 ; 🔴 0 for performance
r.lumen.translucencyvolume.hardwareraytracing=0 ;
r.lumen.translucencyvolume.radiancecache.probeatlasresolutioninprobes=128 ;
r.lumenscene.directlighting.hardwareraytracing=1 ;
r.lumenscene.directlighting.offscreenshadowing.tracemeshsdfs=0 ; 🔴 0 for performance
r.lumenscene.farfield.maxtracedistance=100000 ; 🔴 100000 for performance
r.lumenscene.farfield=0 ;
r.lumenscene.lighting.asynccompute=1 ;
r.lumenscene.radiosity.hardwareraytracing=1 ;
r.lumenscene.radiosity.probeocclusion=0 ; 🔴 0 for performance
r.manylights.hardwareraytracing=1 ;
r.maxanisotropy=16 ; 🔴 0,4,8 for performance
r.minscreenradiusforlights=0.03 ; 🔴 0.06,0.04 for performance
r.motionblurquality=0 ;
r.nanite.asyncrasterization.shadowdepths=1 ;
r.nanite.asyncrasterization=1 ;
r.nanite.streaming.asynccompute=1 ;
r.nanite.streaming.imposters=0 ;
r.nanite.viewmeshlodbias.min=-2 ;
r.nanite.viewmeshlodbias.offset=0 ;
r.ngx.dlss.autoexposure=1 ;
r.ngx.dlss.denoisermode=1 ;
r.ngx.dlss.dilatemotionvectors=1 ;
r.ngx.dlss.enable=1 ;
r.ngx.dlss.prefernissharpen=0 ;
r.ngx.dlss.quality.auto=0 ;
r.ngx.dlss.reflections.temporalaa=0 ;
r.ngx.dlss.sharpness=0 ;
r.ngx.dlss.waterreflections.temporalaa=0 ;
r.ngx.loglevel=0 ;
r.nis.enable=0 ;
r.nis.sharpness=0 ;
r.numbufferedocclusionqueries=2 ;
r.optimizedwpo=1 ;
r.particlelightquality=2 ; 🔴 0,1 for performance
r.pathtracing=0 ; 🔴 0 for performance
r.postprocessaaquality=6 ;
r.postprocessing.prefercompute=1 ;
r.raytracing.ambientocclusion=0 ;
r.raytracing.excludedecals=1 ;
r.raytracing.excludesky=1 ;
r.raytracing.excludetranslucent=1 ;
r.raytracing.geometry.cable=0 ;
r.raytracing.geometry.hierarchicalinstancedstaticmesh=0 ;
r.raytracing.geometry.instancedstaticmeshes.evaluatewpo=0 ;
r.raytracing.geometry.instancedstaticmeshes=0 ;
r.raytracing.geometry.landscape=0 ;
r.raytracing.geometry.landscapegrass=0 ;
r.raytracing.geometry.naniteproxies=1 ;
r.raytracing.geometry.niagarameshes=0 ;
r.raytracing.geometry.niagararibbons=0 ;
r.raytracing.geometry.niagarasprites=0 ;
r.raytracing.geometry.proceduralmeshes=0 ;
r.raytracing.geometry.skeletalmeshes=0 ;
r.raytracing.geometry.splinemeshes=0 ;
r.raytracing.geometry.staticmeshes=1 ;
r.raytracing.globalillumination=0 ;
r.raytracing.lightfunction=0 ;
r.raytracing.nanite.mode=0 ;
r.raytracing.reflections=0 ;
r.raytracing.shadows.acceptfirsthit=1 ;
r.raytracing.shadows.denoiser=0 ; 🔴 0 for performance
r.raytracing.shadows.enablehairvoxel=0 ;
r.raytracing.shadows.enablematerials=0 ;
r.raytracing.shadows.enabletwosidedgeometry=0 ;
r.raytracing.shadows.lights.directional=0 ;
r.raytracing.shadows.lights.point=0 ;
r.raytracing.shadows.lights.rect=0 ;
r.raytracing.shadows.lights.spot=0 ;
r.raytracing.shadows.maxbatchsize=8 ;
r.raytracing.shadows.tiledprojection.downsamplemode=0 ;
r.raytracing.shadows.tiledprojection.filter=1 ;
r.raytracing.shadows.tiledprojection=1 ;
r.raytracing.shadows=0 ; 🔴 0 for performance
r.raytracing.skylight=0 ;
r.raytracing.translucency=0 ;
r.raytracing.usetexturelod=0 ;
r.raytracing=0 ; 🔴 0 for performance
r.reflectioncapturesupersamplefactor=1 ;
r.refraction.blur.temporalaa=1 ;
r.refractionquality=2 ; 🔴 0,1 for performance
r.scenecolorformat=3 ; 🔴 2,3 for performance
r.scenecolorfringe.max=0 ;
r.scenedepthhzbasynccompute=1 ;
r.screenpercentage.maxresolution=0 ;
r.screenpercentage.minresolution=0 ;
r.secondaryscreenpercentage.gameviewport=0 ;
r.shaders.removedeadcode=1 ;
r.shaders.removeunusedinterpolators=1 ;
r.shadow.cachedshadowscastfrommovableprimitives=0 ; 🔴 0 for performance
r.shadow.csm.maxcascades=2 ; 🔴 2 for performance
r.shadow.csm.transitionscale=1 ;
r.shadow.csmshadowdistancefadeoutmultiplier=1 ;
r.shadow.forcesinglesampleshadowingfromstationary=1 ; 🔴 1 for performance
r.shadow.maxcsmresolution=2048 ; 🔴 512,1024 for performance
r.shadow.maxresolution=2048 ; 🔴 512,1024 for performance
r.shadow.nanitelodbias=1 ; 🔴 1 for performance
r.shadow.preshadowresolutionfactor=0.5 ;
r.shadow.radiusthreshold=0.04 ; 🔴 0.06,0.05,0.04 for performance
r.shadow.virtual.clipmap.firstlevel=6 ;
r.shadow.virtual.enable=1 ; 🔴 0 for performance
r.shadow.virtual.forceonlyvirtualshadowmaps=0 ;
r.shadow.virtual.maxphysicalpages=4096 ;
r.shadow.virtual.nonnanite.includeincoarsepages=0 ; 🔴 0 for performance
r.shadow.virtual.nonnanitevsm=1 ; 🔴 0 for performance
r.shadow.virtual.optimalslopebiasmultiplier.directional=0 ;
r.shadow.virtual.resolutionlodbiasdirectional=-1.5 ;
r.shadow.virtual.resolutionlodbiaslocal=0 ;
r.shadow.virtual.smrt.maxrayanglefromlight=0.03 ;
r.shadow.virtual.smrt.raycountdirectional=4 ;
r.shadow.virtual.smrt.raycountlocal=2 ;
r.shadow.virtual.smrt.raylengthscaledirectional=1.5 ;
r.shadow.virtual.smrt.samplesperraydirectional=1 ;
r.shadow.virtual.smrt.samplesperrayhair=1 ;
r.shadow.virtual.smrt.samplesperraylocal=1 ;
r.shadow.virtual.smrt.texelditherscaledirectional=1 ;
r.shadow.virtual.smrt.texelditherscalelocal=1 ;
r.shadow.virtual.subsurfaceshadowmode=1 ;
r.shadow.virtual.translucentquality=0 ; 🔴 0 for performance
r.shadow.virtual.viewbias.directional=0 ;
r.shadowquality=4 ; 🔴 3,4 for performance
r.skyatmosphere.fastskylut.samplecountmax=64 ; 🔴 32 for performance
r.skyatmosphere.fastskylut.samplecountmin=4 ; 🔴 1 for performance
r.skyatmosphere.lut32=0 ; 🔴 0 for performance
r.skyatmosphere.multiscatteringlut.highquality=0 ; 🔴 0 for performance
r.skyatmosphere.multiscatteringlut.samplecount=15 ;
r.skyatmosphere.samplecountmax=64 ; 🔴 32 for performance
r.skyatmosphere.samplecountmin=4 ; 🔴 1 for performance
r.skyatmosphere.samplelightshadowmap=0 ; 🔴 0 for performance
r.skyatmosphere.transmittancelut.samplecount=10 ;
r.skyatmosphere.transmittancelut.usesmallformat=0 ; 🔴 1 for performance
r.skyatmosphereasynccompute=1 ;
r.ssgi.enable=0 ; 🔴 0 for performance
r.ssr.experimentaldenoiser=0 ;
r.ssr.halfresscenecolor=1 ; 🔴 1 for performance
r.ssr.quality=2 ; 🔴 0,2 for performance
r.sss.burley.quality=0 ; 🔴 0 for performance
r.sss.checkerboard=1 ; 🔴 1 for performance
r.sss.halfres=1 ; 🔴 1 for performance
r.streaming.amortizecputogpucopy=0 ;
r.streaming.boost=1 ;
r.streaming.fullyloadusedtextures=0 ;
r.streaming.hiddenprimitivescale=0.5 ; 🔴 0.5 for performance
r.streaming.limitpoolsizetovram=1 ;
r.streaming.maxeffectivescreensize=0 ;
r.streaming.maxnumtexturestostreamperframe=0 ;
r.streaming.mipbias=0 ; 🔴 1 for performance
r.streaming.poolsize.vrampercentageclamp=1024 ;
r.streaming.poolsize=1000 ;
r.streaming.poolsizeformeshes=-1 ;
r.streaming.useallmips=0 ;
r.streaming.usefixedpoolsize=0 ;
r.streaming.usepertexturebias=1 ;
r.subsurfacescattering=1 ; 🔴 0 for performance
r.supportmateriallayers=1 ; 🔴 0 for performance
r.temporalaa.algorithm=0 ;
r.temporalaa.quality=2 ;
r.temporalaa.upsampling=1 ; 🔴 0 for performance
r.temporalaasamples=8 ;
r.tessellationadaptivepixelspertriangle=999999 ; 🔴 999999,48 for performance
r.tonemapper.sharpen=0 ;
r.translucencylightingvolumedim=64 ; 🔴 32,48 for performance
r.translucencyvolumeblur=1 ; 🔴 0 for performance
r.upscale.quality=3 ;
r.volumetriccloud.distancetosamplemaxcount=15 ;
r.volumetriccloud.enableatmosphericlightssampling=1 ;
r.volumetriccloud.enabledistantskylightsampling=1 ;
r.volumetriccloud.enablelocallightssampling=0 ; 🔴 0 for performance
r.volumetriccloud.shadow.sampleatmosphericlightshadowmap=0 ; 🔴 0 for performance
r.volumetriccloud.shadowmap.spatialfiltering=1 ;
r.volumetriccloud.shadowmap=1 ;
r.volumetriccloud.skyao=1 ;
r.volumetriccloud=1 ; 🔴 0 for performance
r.volumetricfog.conservativedepth=0 ;
r.volumetricfog.depthdistributionscale=32 ; 🔴 16 for performance
r.volumetricfog.emissive=0 ;
r.volumetricfog.gridpixelsize=16 ; 🔴 24,16 for performance
r.volumetricfog.gridsizez=96 ; 🔴 64,96 for performance
r.volumetricfog.historymisssupersamplecount=2 ; 🔴 2 for performance
r.volumetricfog.injectraytracedlights.locallights=0 ;
r.volumetricfog.injectraytracedlights=0 ;
r.volumetricfog.jitter=1 ;
r.volumetricfog.lightfunction=0 ;
r.volumetricfog.temporalreprojection=1 ;
r.volumetricfog.upsamplejittermultiplier=0 ; 🔴 0 for performance
r.volumetricfog.useslightfunctionatlas=0 ;
r.volumetricfog=1 ; 🔴 0 for performance
r.volumetricrendertarget.preferasynccompute=1 ;
r.vrs.enable=0 ;
r.vrs.enableimage=0 ;
r.vrs.enablesoftware=0 ;
r.vsync=0 ;
r.vsyncinformationinsights=0 ;
r.vt.anisotropicfiltering=1 ; 🔴 0 for performance
r.vt.maxanisotropy=8 ; 🔴 4 for performance
r.vulkan.allowasynccompute=1 ;
r.water.enableshallowwatersimulation=0 ; 🔴 0 for performance
r.water.enableunderwaterpostprocess=0 ; 🔴 0 for performance
r.water.reflections.maxroughnesstotrace=0.6 ;
r.water.singlelayer.dampenskylight=0 ;
r.water.singlelayer.depthprepass=1 ;
r.water.singlelayer.distancefieldshadow=0 ;
r.water.singlelayer.downsamplereflections=1 ; 🔴 1 for performance
r.water.singlelayer.reflection=1 ; 🔴 0 for performance
r.water.singlelayer.refractiondownsamplefactor=1 ; 🔴 1,2 for performance
r.water.singlelayer.rtr=0 ;
r.water.singlelayer.shaderssupportdistancefieldshadow=0 ;
r.water.singlelayer.shaderssupportvsmfiltering=0 ;
r.water.singlelayer.ssr=0 ; 🔴 0 for performance
r.water.singlelayer.tiledcomposite=1 ;
r.water.singlelayer.underwaterfogwhencameraisabovewater=0 ;
r.water.singlelayer.vsmfiltering=0 ;
r.water.watermesh.tessfactorbias=0 ; 🔴 -1 for performance
r.xess.enabled=0 ;
rhi.maximumframelatency=1 ;
t.maxfps=0 ;
t.overridefps=0 ;
t.streamline.reflex.enable=1 ;
```

---

## open input.ini and copy pasta %localappdata%

```python
[/script/engine.inputsettings]
baltentertogglesfullscreen=1 ;
benablemousesmoothing=0 ;
bf11togglesfullscreen=0 ;
buttonrepeatdelay=0.1 ;
bviewaccelerationenabled=0 ;
doubleclicktime=0.01 ; 🔴 default is 0.1
initialbuttonrepeatdelay=0.1 ; 🔴 default is 0.2
```

---

## ect

```python
## upscaling to use
2560x1440 use 🔴 58%,67%,70% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3328x1872 use 🔴 50%,58%,67% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)
3840x2160 use 🔴 33%,50%,58%,67% for performance (higher when cpu bound) (dlss/taau/tsr/cas/fsr/xess/pssr/nis/is)

## repak.bat method
zzz_inimods\engine\config\windows\windowsengine.ini
zzz_inimods\engine\config\windows\windowsinput.ini
```

---
