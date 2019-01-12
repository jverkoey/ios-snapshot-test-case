# Copyright 2019-present The Material Foundation Authors. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@bazel_ios_warnings//:strict_warnings_objc_library.bzl", "strict_warnings_objc_library")
load(":apple_framework_relative_headers.bzl", "apple_framework_relative_headers")


IOS_MINIMUM_OS = "8.0"

objc_library(
    name = "SnapshotTestCase",
    srcs = native.glob([
        "FBSnapshotTestCase/*.m",
        "FBSnapshotTestCase/Categories/*.m",
    ]),
    hdrs = native.glob([
        "FBSnapshotTestCase/*.h",
        "FBSnapshotTestCase/Categories/*.h",
    ]),
    enable_modules = 1,
    visibility = ["//visibility:public"],
    deps = [":SnapshotTestCaseFrameworkHeaders",],
)

apple_framework_relative_headers(
    name = "SnapshotTestCaseFrameworkHeaders",
    hdrs = native.glob([
        "FBSnapshotTestCase/*.h",
        "FBSnapshotTestCase/Categories/*.h",
    ]),
    framework_name = "FBSnapshotTestCase",
)
