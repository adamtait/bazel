package(default_visibility = ["//src:__subpackages__"])

java_binary(
    name = "xcodegen",
    srcs = glob(["java/**/XcodeGen.java"]),
    main_class = "com.google.devtools.build.xcode.xcodegen.XcodeGen",
    visibility = ["//visibility:public"],
    deps = [
        ":xcodegen_lib",
        "//src/main/java:options",
        "//src/main/protobuf:proto_xcodegen",
        "//third_party:guava",
        "//third_party:protobuf",
        "//third_party/java/buck-ios-support",
    ],
)

java_library(
    name = "xcodegen_lib",
    srcs = glob(
        ["java/**/*.java"],
        exclude = [
            "java/**/XcodeGen.java",
            "java/**/testing/*.java",
        ],
    ),
    deps = [
        "//src/main/protobuf:proto_xcodegen",
        "//src/objc_tools/plmerge:plmerge_lib",
        "//src/tools/xcode-common/java/com/google/devtools/build/xcode/common",
        "//src/tools/xcode-common/java/com/google/devtools/build/xcode/util",
        "//third_party:guava",
        "//third_party:jsr305",
        "//third_party:protobuf",
        "//third_party/java/buck-ios-support",
        "//third_party/java/dd_plist",
    ],
)
