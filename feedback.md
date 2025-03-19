Feedback:

# additional
thetadog.io is not available
"datafeed" and "charting" will be skipped, it seems as an external lib.

# Summary:
The existing project is written as an example of a template implementation with some functionality added. Perhaps this is an early version of the MVP?

All the code does not assume some internal code style guide, but follows JS programming rules.

The diverse coding style gives the feeling that the code base was created by more than one person, or parts of the code were copied from different sources.

The existing codebase is not ready for publication because of hard-coded specific (local) settings.

Due to lack of documentation, it is not clear whether this MVP solves its own goals or not. Overall, it does not implement much functionality - some endpoints are not implemented or mocked.

# remarks:
1. Many url's are hardcoded, to publish a project - requires “shotgun surgery”, Env is not used
2. Strange handling of constant seed values for random number library. Doesn't affect security, but seems more complicated than enough.
3. Missing text translation “pattern”. Other UI languages are impossible without a complete refactoring.
4. Strange validation rules in forms, hard-coded, not organized (duplication of the same rule).
5. Error handlers don't catch possible standard exceptions: e.g. 403 (not enough permissions).
6. Strange hard-coded caching rules for tokens: e.g. Fix 5days. But JWT is open, it can be calculated - how long it should be kept.
7. Built-in reusable model definitions/declarations should be extracted for reuse in automated tasks like testing, etc.
8. Some debug lines in the code, they should probably be wrapped for DEBUG to avoid this in production. But I don't know how this is planned to be published.
9. ES6 syntax is preferred (but not required)
10. Strange management of server-side data validation, it may be reasonable to solve it via Models+Validators.
11. Constant images can be stored locally in static folder.
12. Because of multiple definitions - Router urls should be extracted because it can be better understood.
13. Some object attributes do not conform to JS code standards
14. Server state errors could be more declarative.
15. html theme could be more modern, it seems very outdated.
16. Different ways of working with axios. Perhaps the code was written by several different developers?
17. UI components don't always follow the “components” structure.
18. Hardcoded inline css styles can be refactored for easier style switching. In general - too much css inline instead of classes (subjective opinion).
19. RE-invented html layout breakpoints... maybe it would be better to use Bootstrap?
20. Too much html copy-paste - could be refactored in components.
21. Project seems untestable.
22. Dependencies or external Libraries are very outdated, it is hard to create a dev environment.
23. Project have 44 vulnerabilities (3 low, 22 moderate, 18 high, 1 critical), mongoose is the most outdated library.



# How to decide if further development is planned.

1. Document milestones/goals and mark completed tasks.
2. Document and implement a code style guide, e.g. with babel rules.
3. UI could be better organized by component.
4. For UI, it is better to avoid inline css styles, and maybe start using the MD css library more widely.
5. The server side should be better organized because of the rapid increasing complexity.
6. Need to add basic tests now, for development and add more tests before publishing.
7. Refactoring of Env constants is needed before testing/publishing.
8. Hard refactoring is necessary if there is a goal to switch styles / apply skins
9. Hard/impossible refactoring is required if there is a goal of language switching
10. An improved Readme, even more so a good documentation about the project itself, is highly desirable.