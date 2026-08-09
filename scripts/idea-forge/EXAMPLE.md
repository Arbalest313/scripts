# Example behavior

User:

> I want to build something with WiFi sensing and an LLM that makes a home feel more emotionally aware.

Idea Forge should **not** immediately ask a generic requirements question.

A good first turn would look roughly like:

---

My working interpretation: the interesting part is not "detect motion with WiFi"; it is turning invisible spatial signals into a feeling that the home understands what is happening without cameras.

Three directions worth testing:

1. **The home notices absence, not activity.**
   The product recognizes changes from normal household rhythms and expresses "something feels different" rather than pretending to know exactly what happened.
   Tradeoff: emotionally compelling, but less concrete.

2. **The home becomes a narrator for pets.**
   WiFi sensing detects patterns around sleeping, pacing, waiting, and room-to-room movement; the LLM translates them into small, human-readable moments.
   Tradeoff: much clearer product hook, but pet-state inference can easily overclaim.

3. **The interface disappears.**
   Instead of a dashboard, the system creates ambient outputs: a small light, a daily sentence, or a room-level "memory" of the day.
   Tradeoff: more magical, but harder to explain and validate.

I would start with **#2 + #3**: a very narrow pet story, delivered through an emotional ambient interface, gives you something users can feel before you solve general "smart home intelligence."

**Decision:** What is the first magic moment?

**My recommendation:** The owner comes home and sees one sentence that makes them feel "the house noticed my dog while I was gone"—without claiming a medical or emotional diagnosis.

**Question:** Should that first magic moment be about **reassurance**, **discovery**, or **connection**?

---

The skill then waits for the answer and follows the decision tree one question at a time.
