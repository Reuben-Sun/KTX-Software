# Copyright 2015-2023 The Khronos Group Inc.
# Copyright 2022-2023 RasterGrid Kft.
# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.15)

set(KTX_MAIN_SRC
    include/KHR/khr_df.h
    include/ktx.h
    lib/basis_sgd.h
    lib/basis_transcode.cpp
    lib/miniz_wrapper.cpp
    lib/basisu/transcoder/basisu_containers.h
    lib/basisu/transcoder/basisu_containers_impl.h
    lib/basisu/transcoder/basisu_file_headers.h
    lib/basisu/transcoder/basisu_transcoder_internal.h
    lib/basisu/transcoder/basisu_transcoder_uastc.h
    lib/basisu/transcoder/basisu_transcoder.cpp
    lib/basisu/transcoder/basisu_transcoder.h
    lib/basisu/transcoder/basisu.h
    lib/basisu/zstd/zstd.c
    lib/checkheader.c
    lib/dfdutils/createdfd.c
    lib/dfdutils/colourspaces.c
    lib/dfdutils/dfd.h
    lib/dfdutils/interpretdfd.c
    lib/dfdutils/printdfd.c
    lib/dfdutils/queries.c
    lib/dfdutils/vk2dfd.c
    lib/dfdutils/vk2dfd.inl
    lib/dfdutils/vulkan/vk_platform.h
    lib/dfdutils/vulkan/vulkan_core.h
    lib/etcdec.cxx
    lib/etcunpack.cxx
    lib/filestream.c
    lib/filestream.h
    lib/formatsize.h
    lib/gl_format.h
    lib/hashlist.c
    lib/info.c
    lib/ktxint.h
    lib/memstream.c
    lib/memstream.h
    lib/strings.c
    lib/swap.c
    lib/texture.c
    lib/texture.h
    lib/texture2.c
    lib/texture2.h
    lib/uthash.h
    lib/vk2gl.h
    lib/vk_format.h
    lib/vkFormat2glFormat.inl
    lib/vkFormat2glInternalFormat.inl
    lib/vkFormat2glType.inl
    lib/vkformat_check.c
    lib/vkformat_enum.h
    lib/vkformat_str.c
    lib/vkformat_typesize.c
    )

# Main library
add_library(ktx SHARED ${KTX_MAIN_SRC})

target_include_directories(ktx PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")
