# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  User <|-- Phrases 
  class User {
      + User ID
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
        + TypingTest test
  }
  Phrases <|-- TypingTest
  class Phrases{
        - phrases vector~string~
        + add_phrase(title: string)
        + get_phrases() vector~string~
  }

TypingTest <|-- Accuracy
  class TypingTest{
      startTime(start:float)
      endTime(end:float)
      Accuracy
  }

  class Accuracy {
      - calculate_acc(wpm: float)
      + get_acc() float
      + correctKeystroke(cks: int)
      + getcorrectKeystroke()
  }
```
