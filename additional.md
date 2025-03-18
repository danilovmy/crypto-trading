# additional
"datafeed" and "charting" will be skipped, it seems as an external lib.


# suggestions:
1. Many url hardcoded to publish official - required "shotgun surgery", Env not used
2. Strange works with constant seed values for random library. Not affects on security, but seems more complex than enough.
3. Skipped Text Translations "pattern". Other UI languages not possible without full refactoring.
4. Strange Validation rules in forms, hardcoded, not organized (duplicated the same rule).
5. Error handlers not catch possible standard exceptions: f.e. 403 (not enough permissions).
6. Strange hardcoded caching rules for tokens: f.e. Fix 5days. But JWT is open, it can be calculated - how long it should be stored.
7. inline reusable Model definition/declaration should be extracted for reusing in automated tasks like testing etc.
8. Some debugging staff hardcoded, probably should be decorated to avoid it in production. I don't know how it planned to publish.
9. Syntax ES6 more preferable to use (but not required)
10. Strange organizing server Data validation, probably should be solved through Models+Validators.
11. Constant images can be stored locally in static folder.
12. Due multiple definitions - Router urls should be extracted, because it can be better understand.
13. some object attributes not aligns JS code standards
14. Server status errors can be more declarative.
15. html theme can be more modern, it seems very robust.
16. different arts in works with axios. Probably multiple different authors?
17. Ui components don't always follow "components" structure.
18. Hardcoded inline css styles can be refactored for easier style switching. In general - too much css inline instead of classes (subjective opinion).
19. Reinvented layouts breakpoints.. may be use Bootstrap is better?
20. too much html copy-paste - can be refactored in components.
21. Project seems not testable.

# Summary:
Existed project is written as an example of template implementation with added some functionality. Probably earlier version of MVP?

Whole code not suggest some internal code style guide but follows JS programming rules.

Accordingly different coding arts it seems, that not one person created the codebase, or parts of code was copied from different sources.

Existed codebase not ready for publishing, due hard encoded specific (local) settings.

Due lack of documentations it is not clear, if this codebase solves own goals or not. in general it realized not to much functionality - some endpoints are not realized or mocked.

# How to solve, if it planned to develop further.

1. Document milestones / goals and mark already finished tasks.
2. Document and Implement code-style-guide, f.e. with babel rules.
3. UI can be better organized by components.
4. For UI is Better to avoid css inline styles, and, probably, start to use MD css library wider.
5. Server part should be well organized due fast growing of complexity.
6. Adding basic tests now, for development an additional tests before publishing.
7. Env constants Refactoring needed before testing/publishing.
8. Hard refactoring needed if exists goal on switching styles / applying skins
9. Hard/impossible refactoring needed if exists goal on switching languages
10. Better Readme, even more, good documentation about project itself are hard wanted.

