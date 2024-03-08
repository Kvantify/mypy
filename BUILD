py_library(
    name = "lib",
    srcs = glob([
        "mypy/**/*.py",
    ]),
    data = glob(
        ["mypy/**/*"],
        exclude = ["mypy/**/*.py"],
    ),
    imports = ["."],
    visibility = ["//visibility:public"],
    deps = [
        "@python_deps_mypy_extensions//:pkg",
        "@python_deps_tomli//:pkg",
        "@python_deps_typing_extensions//:pkg",
    ],
)

py_binary(
    name = "bin",
    srcs = ["main.py"],
    main = "main.py",
    visibility = ["//visibility:public"],
    deps = [":lib"],
)
