package(default_visibility = ["//visibility:public"])
cc_library(
    name = "py_executor",
    hdrs = ["py_executor.h"],
    srcs = ["py_executor.cc"],
    copts = [
        "-fvisibility=hidden"
    ],
    deps = [
        "//src/primihub/common:common_defination",
        "//src/primihub/protos:worker_proto",
        "@com_github_base64_cpp//:base64_lib",
        "@pybind11",
        "@com_google_absl//absl/base",
        "@com_google_absl//absl/flags:flag",
        "@com_google_absl//absl/flags:parse",
        "@com_google_absl//absl/memory",
        "@com_github_glog_glog//:glog",
    ],
)

cc_library(
    name = "mpc_express_executor",
    hdrs = ["express.h"],
    srcs = ["express.cc"],
    deps = [
        "//src/primihub/operator:aby3_operator",
        "@com_github_glog_glog//:glog"
    ],
)
