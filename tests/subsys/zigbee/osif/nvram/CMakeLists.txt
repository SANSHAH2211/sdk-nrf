#
# Copyright (c) 2020 Nordic Semiconductor ASA
#
# SPDX-License-Identifier: LicenseRef-BSD-5-Clause-Nordic
#

cmake_minimum_required(VERSION 3.13.1)

# Stub for ZBOSS callout
add_compile_definitions(zb_nvram_erase_finished=zb_nvram_erase_finished_stub)

include($ENV{ZEPHYR_BASE}/../nrf/cmake/boilerplate.cmake)
find_package(Zephyr HINTS $ENV{ZEPHYR_BASE})

project(zigbee_osif_nvram_test)

target_sources(app PRIVATE
  src/main.c
)
