
CMAKE_MINIMUM_REQUIRED(VERSION 2.6 FATAL_ERROR)
CMAKE_POLICY(VERSION 2.6)
FIND_PACKAGE(Torch REQUIRED)

SET(luasrc init.lua 
    AutoEncoder.lua
    LinearFistaL1.lua 
    SpatialConvFistaL1.lua 
    psd.lua
    LinearPsd.lua
    ConvPsd.lua
    UnsupModule.lua
    UnsupTrainer.lua
    pca.lua
    kmeans.lua
    test/test_fista.lua)

ADD_TORCH_PACKAGE(unsup ""  "${luasrc}" "Unsupervised Learning")
