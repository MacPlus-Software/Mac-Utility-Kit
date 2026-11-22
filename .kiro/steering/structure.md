# Architecture boundaries

`Foundation/MacUtilityKit` owns reusable menu-bar app shell primitives, shared preferences abstractions, reusable settings/popup components, and testable small helpers as warranted.

`Apps/CleanPaste` owns clipboard access, text transformations, before/after UX, and copy action.

`Apps/FocusTick` owns timer state, start/pause/reset commands, and optional user-authorized notifications.

Avoid a shared module that contains app-specific business logic. Define app-specific services with dependency injection where appropriate. Ensure each app runs independently. The two app folders must remain visible in the repository for judging.
