#############################################
#  CMakeLists.txt file for SPOOLES sources
#############################################

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}/../include
  )

set(A2_SRCS
  A2/IO.c
  A2/QRreduce.c
  A2/basics.c
  A2/copyEntriesToVector.c
  A2/init.c
  A2/instance.c
  A2/makeStaircase.c
  A2/norms.c
  A2/sort.c
  A2/util.c
  )

set(BKL_SRCS
  BKL/basics.c
  BKL/evalfcn.c
  BKL/exhSearch.c
  BKL/fidmat.c
  BKL/init.c
  BKL/util.c
  )

set(BPG_SRCS
  BPG/DM.c
  BPG/IO.c
  BPG/basics.c
  BPG/init.c
  BPG/makeGraphs.c
  BPG/maxFlow.c
  BPG/pseudo.c
  CMakeLists.txt
  )

set(Chv_SRCS
  Chv/IO.c
  Chv/assemble.c
  Chv/basics.c
  Chv/copy.c
  Chv/factor.c
  Chv/findPivot.c
  Chv/init.c
  Chv/instance.c
  Chv/search.c
  Chv/swap.c
  Chv/update.c
  Chv/util.c
  )

set(ChvList_SRCS
  ChvList/IO.c
  ChvList/basics.c
  ChvList/init.c
  ChvList/util.c
  ChvManager
  ChvManager/IO.c
  ChvManager/basics.c
  ChvManager/init.c
  ChvManager/util.c
  )

set(Coords_SRCS
  Coords/IO.c
  Coords/basics.c
  Coords/init.c
  Coords/util.c
  )

set(DSTree_SRCS
  DSTree/IO.c
  DSTree/basics.c
  DSTree/init.c
  DSTree/instance.c
  DSTree/stages.c
  DSTree/util.c
  )

set(DV_SRCS
  DV/IO.c
  DV/basics.c
  DV/init.c
  DV/instance.c
  DV/profile.c
  DV/util.c
  )

set(DenseMtx_SRCS
  DenseMtx/IO.c
  DenseMtx/basics.c
  DenseMtx/init.c
  DenseMtx/initAsSubmtx.c
  DenseMtx/instance.c
  DenseMtx/permute.c
  DenseMtx/scale.c
  DenseMtx/util.c
  )

set(Drand_SRCS
  Drand/basics.c
  Drand/init.c
  Drand/util.c
  )

set(EGraph_SRCS
  EGraph/IO.c
  EGraph/basics.c
  EGraph/init.c
  EGraph/misc.c
  EGraph/mkAdjGraph.c
  )

set(ETree_SRCS
  ETree/IO.c
  ETree/basics.c
  ETree/compress.c
  ETree/init.c
  ETree/initFromSubtree.c
  ETree/instance.c
  ETree/justify.c
  ETree/maps.c
  ETree/metrics.c
  ETree/ms.c
  ETree/permute.c
  ETree/semi.c
  ETree/storage.c
  ETree/transform.c
  ETree/util.c
  )

set(FrontMtx_SRCS
  FrontMtx/IO.c
  FrontMtx/QRfactor.c
  FrontMtx/QRsolve.c
  FrontMtx/QRutil.c
  FrontMtx/basics.c
  FrontMtx/factor.c
  FrontMtx/factorUtil.c
  FrontMtx/init.c
  FrontMtx/instance.c
  FrontMtx/loadEntries.c
  FrontMtx/permute.c
  FrontMtx/postProcess.c
  FrontMtx/postponed.c
  FrontMtx/solve.c
  FrontMtx/solveUtil.c
  FrontMtx/split.c
  FrontMtx/storeFront.c
  FrontMtx/update.c
  FrontMtx/util.c
  )

set(GPart_SRCS
  GPart/DDsepInfo.c
  GPart/DDsepInfo.h
  GPart/DDviaFishnet.c
  GPart/DDviaProjection.c
  GPart/RBviaDDsep.c
  GPart/TwoSetViaBKL.c
  GPart/basics.c
  GPart/domSegMap.c
  GPart/identifyWideSep.c
  GPart/init.c
  GPart/makeYCmap.c
  GPart/smoothBisector.c
  GPart/smoothBy2layers.c
  GPart/smoothYSep.c
  GPart/split.c
  GPart/util.c
  )

set(Graph_SRCS
  Graph/IO.c
  Graph/basics.c
  Graph/compress.c
  Graph/equivMap.c
  Graph/expand.c
  Graph/fillFromOffsets.c
  Graph/init.c
  Graph/setListsFromOffsets.c
  Graph/util.c
  Graph/wirebasket.c
  )

set(I2Ohash_SRCS
  I2Ohash/IO.c
  I2Ohash/basics.c
  I2Ohash/init.c
  I2Ohash/util.c
  )

set(IIheap_SRCS IIheap/basics.c)

set(ILUMtx_SRCS
  ILUMtx/IO.c
  ILUMtx/basics.c
  ILUMtx/factor.c
  ILUMtx/init.c
  ILUMtx/misc.c
  ILUMtx/solve.c
  )

set(IV_SRCS
  IV/IO.c
  IV/basics.c
  IV/init.c
  IV/instance.c
  IV/util.c
  )

set(IVL_SRCS
  IVL/IO.c
  IVL/basics.c
  IVL/init.c
  IVL/instance.c
  IVL/listmanip.c
  IVL/misc.c
  IVL/subIVL.c
  IVL/util.c
  )

set(Ideq_SRCS
  Ideq/IO.c
  Ideq/basics.c
  Ideq/resize.c
  Ideq/util.c
  )

set(InpMtx_SRCS
  InpMtx/IO.c
  InpMtx/adjForATA.c
  InpMtx/basics.c
  InpMtx/extract.c
  InpMtx/fullAdj.c
  InpMtx/gmmm.c
  InpMtx/gmvm.c
  InpMtx/init.c
  InpMtx/input.c
  InpMtx/instance.c
  InpMtx/map.c
  InpMtx/mvm.c
  InpMtx/mvmVector.c
  InpMtx/permute.c
  InpMtx/profile.c
  InpMtx/support.c
  InpMtx/util.c
  )

set(Iter_SRCS
  Iter/DenseMtx_mmm.c
  Iter/bgmresl.c
  Iter/bgmresr.c
  Iter/bicgstabl.c
  Iter/bicgstabr.c
  Iter/mlbicgstabl.c
  Iter/mlbicgstabr.c
  Iter/pcgl.c
  Iter/pcgr.c
  Iter/tfqmrl.c
  Iter/tfqmrr.c
  Iter/util.c
  Iter/zbicgstabl.c
  Iter/zbicgstabr.c
  Iter/zmlbicgstabl.c
  Iter/zmlbicgstabr.c
  Iter/zpcgl.c
  Iter/zpcgr.c
  Iter/ztfqmrl.c
  Iter/ztfqmrr.c
  )

set(Lock_SRCS
  Lock/basics.c
  Lock/init.c
  Lock/util.c
  )

set(MSMD_SRCS
  MSMD/MSMDinfo.c
  MSMD/MSMDvtx.c
  MSMD/basics.c
  MSMD/cleanReachSet.c
  MSMD/eliminate.c
  MSMD/fillPerms.c
  MSMD/findInodes.c
  MSMD/frontETree.c
  MSMD/init.c
  MSMD/makeSchurComplement.c
  MSMD/order.c
  MSMD/update.c
  )

set(MT_SRCS
  MT/QRfactorMT.c
  MT/QRsolveMT.c
  MT/factorMT.c
  MT/mvm.c
  MT/solveMT.c
  )

set(Network_SRCS
  Network/IO.c
  Network/addArc.c
  Network/augmentPath.c
  Network/basics.c
  Network/findAugmentingPath.c
  Network/findMaxFlow.c
  Network/findMincut.c
  Network/init.c
  PatchAndGoInfo
  PatchAndGoInfo/basics.c
  PatchAndGoInfo/init.c
  )

set(Pencil_SRCS
  Pencil/IO.c
  Pencil/basics.c
  Pencil/init.c
  Pencil/mmm.c
  Pencil/permute.c
  Pencil/setup.c
  Pencil/util.c
  )

set(Perm_SRCS
  Perm/IO.c
  Perm/basics.c
  Perm/compress.c
  Perm/init.c
  Perm/util.c
  )

set(SemiImplMtx_SRCS
  SemiImplMtx/IO.c
  SemiImplMtx/SemiImplMtx.h
  SemiImplMtx/basics.c
  SemiImplMtx/init.c
  SemiImplMtx/solve.c
  SemiImplMtx/util.c
  )

set(SolveMap_SRCS
  SolveMap/IO.c
  SolveMap/basics.c
  SolveMap/init.c
  SolveMap/instance.c
  SolveMap/maps.c
  SolveMap/setup.c
  SolveMap/util.c
  )

set(SubMtx_SRCS
  SubMtx/IO.c
  SubMtx/basics.c
  SubMtx/init.c
  SubMtx/initRandom.c
  SubMtx/instance.c
  SubMtx/scalevec.c
  SubMtx/solve.c
  SubMtx/solveH.c
  SubMtx/solveT.c
  SubMtx/solveupd.c
  SubMtx/solveupdH.c
  SubMtx/solveupdT.c
  SubMtx/sort.c
  SubMtx/util.c
  )

set(SubMtxList_SRCS
  SubMtxList/IO.c
  SubMtxList/basics.c
  SubMtxList/init.c
  SubMtxList/util.c
  )

set(SubMtxManager_SRCS
  SubMtxManager/IO.c
  SubMtxManager/basics.c
  SubMtxManager/init.c
  SubMtxManager/util.c
  )

set(SymbFac_SRCS SymbFac/symbfac.c)

set(Tree_SRCS
  Tree/IO.c
  Tree/basics.c
  Tree/compress.c
  Tree/draw.c
  Tree/getCoords.c
  Tree/init.c
  Tree/instance.c
  Tree/justify.c
  Tree/maximizeGain.c
  Tree/metrics.c
  Tree/perms.c
  Tree/permute.c
  Tree/subtree.c
  Tree/util.c
  )

set(Utilities_SRCS
  Utilities/CV.c
  Utilities/DV.c
  Utilities/FV.c
  Utilities/I2OP.c
  Utilities/IP.c
  Utilities/IV.c
  Utilities/PCV.c
  Utilities/PDV.c
  Utilities/PFV.c
  Utilities/PIV.c
  Utilities/ZV.c
  Utilities/axpy.c
  Utilities/iohb.c
  Utilities/newsort.c
  Utilities/sortAndCompress.c
  )

set(ZV_SRCS
  ZV/IO.c
  ZV/basics.c
  ZV/init.c
  ZV/instance.c
  ZV/profile.c
  ZV/util.c
  )

set(misc_SRCS
  misc/ND.c
  misc/ND2.c
  misc/drawGraphEPS.c
  misc/fpgrids.c
  misc/localND.c
  misc/mkNDlinsys.c
  misc/mkNDlinsysQR.c
  misc/orderViaBestOfNDandMS.c
  misc/orderViaMMD.c
  misc/orderViaMS.c
  misc/orderViaND.c
  )


set(SPOOLES_SRCS
  ${A2_SRCS} ${BKL_SRCS} ${BPG_SRCS} ${Chv_SRCS} ${ChvList_SRCS} 
  ${Coords_SRCS} ${DSTree_SRCS} ${DV_SRCS} ${DenseMtx_SRCS} 
  ${Drand_SRCS} ${EGraph_SRCS} ${ETree_SRCS} ${FrontMtx_SRCS} 
  ${GPart_SRCS} ${Graph_SRCS} ${I2Ohash_SRCS} ${IIheap_SRCS} 
  ${ILUMtx_SRCS} ${IV_SRCS} ${IVL_SRCS} ${Ideq_SRCS} ${InpMtx_SRCS} 
  ${Iter_SRCS} ${Lock_SRCS} ${MSMD_SRCS} ${MT_SRCS} ${Network_SRCS} 
  ${Pencil_SRCS} ${Perm_SRCS} ${SemiImplMtx_SRCS} ${SolveMap_SRCS} 
  ${SubMtx_SRCS} ${SubMtxList_SRCS} ${SubMtxManager_SRCS} 
  ${SymbFac_SRCS} ${Tree_SRCS} ${Utilities_SRCS} ${ZV_SRCS} 
  ${misc_SRCS})

set(MPI_SRCS
  MPI/DenseMtx_gather.c
  MPI/DenseMtx_scatterAdd.c
  MPI/ETree_Bcast.c
  MPI/Graph_Bcast.c
  MPI/IVL_Bcast.c
  MPI/IVL_alltoall.c
  MPI/IVLallgather.c
  MPI/IV_Bcast.c
  MPI/IVallgather.c
  MPI/MMM.c
  MPI/aggListMPI.c
  MPI/colmapMPI.c
  MPI/factorMPI.c
  MPI/fullAdjMPI.c
  MPI/makeSendRecvIVLs.c
  MPI/postProcess.c
  MPI/rowmapMPI.c
  MPI/solveMPI.c
  MPI/splitDenseMtx.c
  MPI/splitFrontMtx.c
  MPI/splitInpMtx.c
  MPI/splitPencil.c
  MPI/symbfacMPI.c
  MPI/utilities.c
  )

add_library(spooles ${SPOOLES_SRCS})


# Local Variables:
# tab-width: 8
# mode: cmake
# indent-tabs-mode: t
# End:
# ex: shiftwidth=2 tabstop=8


