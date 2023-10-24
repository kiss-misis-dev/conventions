# Global specification

- `game` - эвент клуба интелектуальных игр МИСИС.
- `state` - состояние объекта `game`.
  Возможные состояния:
  - before:
    - `scheduled`
    - `registration open`
    - `registration closed`
  - in progress:
    - `play` - дефолтное состояние эвента, когда ведущий шутейку шутит или правила рассказывает.
    - `round` - внимание, вопрос!
    - `pause` - перерыв на обед
  - after:
  - `verifying` - проверка результатов
  - `closed` - игра завершена! поздравляю, товарищи!

## Components

- `data storage` - микросервис, хранящий информацию о зарегистрированных командах и пользователях, а также о прошедших играх.
- `game server` - микросервис, владеющий состоянием игры.
- `game master` - клиент, упраляющий ходом игры.
- `validator` - клиент, проверяющий и вносящий ответы.
- `presenter` - клиент, отображающий текущее состояние эвента и его компонентов.