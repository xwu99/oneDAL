package(default_visibility = ["//visibility:public"])
load("@onedal//dev/bazel:dal.bzl",
    "dal_module",
    "dal_test_suite",
)

dal_module(
    name = "blas",
    auto = True,
    dal_deps = [
        "@onedal//cpp/oneapi/dal/backend/primitives:common",
    ],
)

dal_test_suite(
    name = "tests",
    private = True,
    framework = "catch2",
    compile_as = [ "dpc++" ],
    srcs = glob([
        "test/*_dpc.cpp",
    ]),
    dal_deps = [
        ":blas",
    ],
)
