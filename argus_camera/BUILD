"""
Copyright (c) 2019, NVIDIA CORPORATION. All rights reserved.

NVIDIA CORPORATION and its licensors retain all intellectual property
and proprietary rights in and to this software, related documentation
and any modifications thereto. Any use, reproduction, disclosure or
distribution of this software and related documentation without an express
license agreement from NVIDIA CORPORATION is strictly prohibited.
"""

load("//bzl:module.bzl", "isaac_app", "isaac_cc_module")

isaac_app(
    name = "argus_camera",
    app_json_file = "argus_camera.app.json",
    modules = [
        "//apps/tutorials/opencv_edge_detection:edge_detector",
        "sensors:argus_camera",
        "sight",
        "viewers",
    ],
    tags = ["manual"],
)
