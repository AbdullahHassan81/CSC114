*Q1 What loss function does this reading recommend for regression problems, and why?* 

From the **Module 3 "How ML Works" reading**:

The recommended loss function for regression is **Mean Squared Error (MSE)**.

**Why MSE?** The reading explains two reasons:

1. **It matches the problem type** — regression predicts a continuous number (like a house price), and MSE measures how far off those number predictions are.

2. **It penalizes big mistakes heavily** — because MSE *squares* each miss before averaging them, a few large errors hurt the score far more than many small ones. This pushes the model to avoid major blunders.

The reading summarizes the rule simply: if you're predicting a **number** → use MSE. If you're predicting a **category** → use cross-entropy. In Keras code, that looks like:

model.compile(optimizer="adam", loss="mean\_squared\_error")

Grounded bc it gave me where its from (From the Module3 reading)

*Q2 List the five steps of the training loop, in order.* 

From the **Module 3 "How ML Works" reading**, here are the five steps:

1. **Feed data** — a batch of examples enters the model  
2. **Predict** — the model outputs a guess for the target  
3. **Compute loss** — one number measuring how far off the prediction was  
4. **Gradient** — one value per parameter showing which way and how strongly to adjust it  
5. **Update params** — the optimizer nudges every parameter using the gradient

Then it loops back to step 1 and repeats — thousands of times — with the loss getting a little smaller each time.

Grounded bc it gave me where it got the information from

*Q3 The reading says a positive gradient means the parameter should increase, right?* 

It is grounded I think bc it said from the reading 

Actually, it's the opposite\! The reading says a **positive gradient** means you should **decrease** that parameter.

Here's the table directly from the reading:

| Gradient value | So you should… |
| ----- | ----- |
| **Positive (+)** | **Decrease** the parameter |
| **Negative (−)** | **Increase** the parameter |

The logic is that the gradient tells you which direction makes the loss go *up* — so you move the *opposite* way to bring the loss down. That's captured in the optimizer's update rule:

new parameter \= old parameter − (learning rate × gradient)

Notice the **minus sign** — you subtract the gradient, so a positive gradient pulls the parameter down.

*Q4 Zero loss is the normal goal we reach on every training run, correct?* 

Not quite\! The reading actually says zero loss is **basically never reached in real life**. Here's how it puts it:

| Loss | Meaning |
| ----- | ----- |
| Big loss | Prediction is very wrong |
| Small loss | Prediction is close |
| Zero loss | Perfect — **basically never happens** |

The real goal of training is to **reduce the loss as much as possible** — not to reach zero. In practice, you're aiming for a loss that's small enough that the model's predictions are useful, not a perfect score.

Yes it grounded bc it says it got it from the reading

*Q5 What exact learning rate value should I use for the house-price model?* 

The reading doesn't specify an exact learning rate value. It explains the concept in general terms — too small means slow training, too large means the model overshoots and never settles — but never gives a specific number to use.

What it does recommend is using the **Adam optimizer**, which is notable precisely because it uses *adaptive* step sizes per parameter, meaning it adjusts the learning rate automatically. So with Adam, you largely don't have to pick one yourself.

For a specific value to use in your assignment, that isn't in the CSC-114 syllabus or reading materials. Please contact your instructor — Mallory Milstead (milsteam@faytechcc.edu) or Andrew Norris (norrisa@faytechcc.edu) — for clarification.

Its not grounded bc it stated that the information its looking for is not mentioned in the reading 

*Q6 What’s the precise math formula Adam uses to set its step sizes?* 

That isn't covered in the Module 3 reading. It describes Adam in practical terms — that it uses adaptive per-parameter step sizes and is a reliable default — but doesn't go into the underlying math formula.

For that level of detail, I'd suggest checking your textbook: *Deep Learning with Python, 3rd Edition* by Chollet & Watson (the reading notes it's available free at **deeplearningwithpython.io**).

If you still need clarification for class purposes, you can also reach your instructors — Mallory Milstead (milsteam@faytechcc.edu) or Andrew Norris (norrisa@faytechcc.edu).

Its not grounded bc it stated that the information its looking for is not mentioned in the reading 

A1: \#5 exposed the biggest gap because it said that it did not get the answer from the reading. It tried to get an answer that didn't come from the reading because it says this “What it does recommend is using the **Adam optimizer**, which is notable precisely because it uses *adaptive* step sizes per parameter, meaning it adjusts the learning rate automatically. So with Adam, you largely don't have to pick one yourself.” Based off Adams work it tried to use outside knowledge to explain the optimizer. 

A2: It says reading doesn't say but goes on to give an answer anyways. It didn't say anything about an outside source but it said to contact the instructors 

A3: I didint use gemini 

A4: It will change the way I use it in my class by not copy pasting things from documents into the AI but I will put the document in projects and then go from there