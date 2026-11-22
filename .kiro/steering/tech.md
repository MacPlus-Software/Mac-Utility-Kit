# Technology and quality constraints

- Swift, SwiftUI, and standard macOS frameworks; AppKit interop only when necessary.
- Shared module as a standard Swift Package in `Foundation/MacUtilityKit`.
- Two separate native macOS app targets in `Apps/CleanPaste` and `Apps/FocusTick`.
- Prefer platform-native UI, accessibility, minimal permissions, and offline-first behavior.
- Keep code free of third-party dependencies unless there is a clear reason.
- Add reproducible macOS build/test instructions once targets exist.
- Do not fabricate test results, screenshots, implementation progress, or Kiro usage.
