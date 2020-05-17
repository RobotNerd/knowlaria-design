# Knowlaria - education game platform

A game-based platform for self-directed education.

## Platform components

- Knowlaria Game
  - An RPG-style video game that acts as the main interface for using the
    system.
- Quiz API
  - Serve quiz questions and validate answers.
  - The question provided depends on the the status of the current user.
    - For example, a novice at math might receive a simple question about
      addition. However, an advanced math user might be served a question
      that involves differential equations.
  - Questions are requested based on a knowledge domain such as math,
    chemistry, history, sociology, etc.
- Story API
  - Dynamically generate in-game stories and missions used by the game.
- User API
  - Track and manage status of a give user.
  - Things that comprise a user's status are.
    - Current skill level per knowledge domain (e.g. ranking at chemistry, math,
      etc.).
    - History of questions answered and the accuracy of the answers.
  - Store and manage user settings and preferences.

## Concerns and Considerations

- Young users
  - This is targeted to users who will be considered minors.
  - The system needs to be a safe space that prevents bad actors (like online
    predators and unscrupulous marketers) from taking advantage of the users
    on the platform.
- User privacy
- GDPR/CCPA
  - A user needs to be able to delete his/her account completely.
- De-platforming
  - A user should be allowed to download information that the platform stores
    about them.
  - The actual question and answer content of the platform is not included.
    The users can download statistical data about the history of how they
    have answered questions.
- Feedback
  - Some question and answer content provided by the system may be wrong or
    only valid within certain cultural contexts.
  - The platform should provide a simple way for users to flag problematic
    question content so that system admins can review this content.
