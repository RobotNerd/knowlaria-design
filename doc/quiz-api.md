# Quiz API

## Route: `/ask`

Retrieve a question for the user.

### Request

```yaml
domain: string # Knowledge domain of the question.
rank: integer # The difficulty level of the question (based on user's ranking).
user: integer # Unique id of user.
```

Example:
```yaml
domain: 'chemistry'
rank: 3
user: 123
```

### Response

```yaml
id: integer # Unique id of this instance of the question.
domain: # Knowledge domain of the question.
question: string # Text of the question.
options: list # (Optional) Multiple choice set of answers to choose from.
  multiselect: boolean # If true, multiple values can be selected.
  - option:
    id: number
    value: string
trueFalse: boolean # (Optional) If true, the answer is either True or False.
```

Example:
```yaml
id: 3343
domain: "earth science"
questions: "Which of the following is true?"
options:
  multiselect: false
  - option:
    id: 1
    value: "The sky is green."
  - option:
    id: 2
    value: "The sky is blue".
  - option:
    id: 3
    value: "There is no sky."
```

Notes
- `trueFalse` and `options` are mutually exclusive.
- If neither `trueFalse` or `options` fields are provided, then an answer
  must be typed in by the user.

## Route: `/answer`

Provide an answer to a question.

### Request

> TODO

### Response

> TODO

### Failure modes:

- Unique id of question not found.
- Time limit to answer question has expired.
