# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  
  User <|-- TypingTest
  class User {
      + User ID
        - name: string
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
        + TypingTest test
        + sessions vector~TypingTest~
  }
  
  class Phrases{
        - phrases vector~string~
        + add_phrase(title: string)
        + get_phrases() vector~string~
  }
TypingTest <|--Phrases
TypingTest
  class TypingTest{
      startTime(start:float)
      endTime(end:float)
      Phrases phrases
      - calculateAccuracy(wpm: float)
      + get_acc() float
      + calculateCorrectKeystrokes(cks: int)
      + getcorrectKeystroke()
  }
  

 
```
