package(default_visibility = ["//visibility:public",],)
C_OPT = []
LINK_OPTS = []
cc_library(
    name = "endian_util",
    hdrs = [
        "endian_util.h",
    ],
)

cc_library(
    name = "instruction_check_util",
    hdrs = [
        "cpu_check.h",
    ],
)

cc_library(
    name = "model_util_lib",
    srcs = glob([
        "model_util.cc",
    ]),
    hdrs = glob([
        "model_util.h",
    ]),
    copts = C_OPT,
    linkopts = LINK_OPTS,
    linkstatic = False,
    deps = [
        ":eigen_util",
        "//src/primihub/common:common_lib",
    ],
)
cc_library(
    name = "file_util",
    hdrs = ["file_util.h"],
    srcs = ["file_util.cc"],
)

cc_library(
    name = "log_util",
    hdrs = ["log.h"],
    srcs = ["log.cc"],
)

cc_library(
    name = "time_util",
    hdrs = ["timer.h"],
    srcs = ["timer.cc"],
    deps = [
        ":log_util",
    ],
)

cc_library(
    name = "util_lib",
    srcs = glob([
        "util.cc",
    ]),
    hdrs = glob([
        "util.h",
    ]),
    copts = C_OPT,
    linkopts = LINK_OPTS,
    linkstatic = False,
    deps = [
        ":file_util",
        ":log_util",
        ":time_util",
        ":threadsafe_queue",
        "//src/primihub/protos:worker_proto",
        "//src/primihub/common:common_lib",
        "@com_github_glog_glog//:glog",
        "@boost//:asio",
        "@boost//:circular_buffer",
    ],
)

cc_library(
    name = "eigen_util",
    hdrs = [
        "eigen_util.h",
    ],
    srcs = [
        "eigen_util.cc",
    ],
    deps = [
        "@eigen//:eigen",
    ],
)

cc_library(
    name = "threadsafe_queue",
    hdrs = ["threadsafe_queue.h",],
)

cc_library(
    name = "redis_helper",
    hdrs = ["redis_helper.h"],
    srcs = ["redis_helper.cc"],
    deps = [
        "@com_github_redis_hiredis//:hiredis",
        "@com_github_glog_glog//:glog",
    ],
)