package(default_visibility = ["//visibility:public",],)
cc_library(
    name = "mysql_driver",
    hdrs = ["mysql_driver.h"],
    srcs = ["mysql_driver.cc"],
    linkopts = [
        "-lmysqlclient",
    ],
    deps = [
        "//src/primihub/data_store:base_driver",
        "//src/primihub/util:util_lib",
        "@arrow",
        "@nlohmann_json",
    ],
)