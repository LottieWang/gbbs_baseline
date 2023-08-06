licenses(["notice"])

cc_library(
    name = "StronglyConnectedComponents",
    hdrs = ["StronglyConnectedComponents.h"],
    deps = [
        "//gbbs",
        "//gbbs/helpers:resizable_table",
    ],
)
cc_binary(
    name = "StronglyConnectedComponents_main",
    srcs = ["StronglyConnectedComponents.cc"],
    deps = [":StronglyConnectedComponents"],
    defines = select({
        "//conditions:default": [],
    }),
)

cc_binary(
    name = "StronglyConnectedComponents_serial_main",
    srcs = ["StronglyConnectedComponents.cc"],
    deps = [":StronglyConnectedComponents"],
    defines = select({
        "//conditions:default": [],
    }),
)

package(
    default_visibility = ["//visibility:public"],
)

