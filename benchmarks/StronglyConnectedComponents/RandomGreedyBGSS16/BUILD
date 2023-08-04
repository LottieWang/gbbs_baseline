licenses(["notice"])

cc_library(
    name = "StronglyConnectedComponents",
    hdrs = ["StronglyConnectedComponents.h"],
    deps = [
        "//gbbs",
        "//gbbs/helpers:resizable_table",
    ],
)
config_setting(
    name = "breakdown_on",
    define_values = {"breakdown": "1"}
)

config_setting(
    name = "breakdown_off",
    define_values = {"breakdown": "0"}
)
cc_binary(
    name = "StronglyConnectedComponents_main",
    srcs = ["StronglyConnectedComponents.cc"],
    deps = [":StronglyConnectedComponents"],
    defines = select({
        ":breakdown_on": ["BREAKDOWN=1"],
        ":breakdown_off": [],
        "//conditions:default": [],
    }),
)

package(
    default_visibility = ["//visibility:public"],
)

