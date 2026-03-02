# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  User <|-- Phrases
  class User {
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class Phrases{
        - phrases vector~string~
        + add_phrase(title: string)
        + get_phrases() vector~string~
  }

  class Accuracy {
      - calculate_acc(wpm: float)
      + get_acc() float
  }
```
