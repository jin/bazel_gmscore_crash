package(
  default_visibility = ["//visibility:public"],
)

filegroup(
  name = "resources",
  srcs = glob(["res/**"]),
)

android_library(
  name = "libbin",
  manifest = "LibManifest.xml",
  srcs = glob(["*.java"]),
  resource_files = [":resources"],
  deps = [
    "@com_google_android_gms_play_services_ads_11_8_0//aar",
    "@com_google_android_gms_play_services_ads_lite_11_8_0//aar",
    "//java/com/example/lib",
  ]
);

android_binary(
  name = "bin",
  manifest = "AndroidManifest.xml",
  srcs = glob(["*.java"]),
  deps = [
    "//java/com/example/lib",
    ":libbin",
  ],
)
