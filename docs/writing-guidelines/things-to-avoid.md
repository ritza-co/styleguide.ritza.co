# Things to avoid

## Avoid giving the reader too many options

Often, there are many ways to achieve the same task. Avoid giving the reader options wherever possible - the reader is looking to you for guidance, so be **opinionated** instead of **comprehensive**.

* ❌ "You can use either the CLI or the GUI. If you prefer the CLI, then type the following command. If you prefer the GUI then click Foo -> Bar.
* ✅ "We recommend using the CLI. Type the following command"

If you really need to show multiple ways of achieiving the same thing, still emphasise the recommended one more than the other (e.g. include the alternative in a footnote or parentheses). It is OK to have a personal preference.

## Avoid getting in the reader’s way:

* ❌ "I wrote this guide after encountering difficulties with the software myself"
* ❌ "Next, I'm going to show you how to install a widget factory"

## Avoid 'marketing' speak.

Never try to sell something to the reader. Don't say a product makes things easy, that a design is beautiful, or use any text that you might find on a SaaS landing page.

## Avoid anything you might find in an encyclopaedia or academic paper.

Your reader isn't interested in definitions - or if they are, they can easily find these elsewhere. 

If you're writing an article on NER, instead of starting with

❌ "Named Entity Recognition (NER) is the task of categorising key words in a text as specific entities."

Consider something more like 

✅ "If you're analyzing a large amount of text, it's often useful to extract named entities from this - identifying people, places, dates and other entities."

If you've ever tried to learn a new concept, you probably already know that reading a definition doesn't really clarify - but a more specific example does.

## Avoid assuming knowledge.

This can be tricky because, of course, you always have to assume _some_ level of knowledge when writing technical content. However, we try to avoid assumptions about our reader's skill level. 

* ❌ "Referring back to the server code, it's obvious that we need both a success.html and a cancel.html."
* ✅ "Referring back to the server code, you may notice it requires both a success.html and a cancel.html."

## Avoid guessing out loud what the reader wants.

It's tempting to start an article with "Are you are a foo who likes to bar but sometimes finds baz?", but this approach defines a narrow audience and you risk alienating anyone who is not a part of it.

## Avoid giving extraneous context.

It's tempting to give the reader related context or information, but your reader is here to achieve a specific goal. Leave out anything that doesn’t help them achieve it.

Instead of:

❌ Label Studio is an open source data labeling tool for labeling and exploring multiple types of data. Label Studio can be integrated with machine learning models to supply predictions for labels (pre-labels), or perform continuous active learning. You can use Label Studio for a variety of labelling and classification tasks for many different data formats but again we will just be focusing on its NER capabilities.

Try something more concise:

✅ We can use Label Studio for manually tagging Named Entities in our dataset. Install it now with `pip install label-studio` if you haven't already.

## Avoid telling the reader that something is obvious or easy.

This discourages the reader who doesn’t find it obvious or easy, and adds no value to the reader who does.

Mostly, `~it's simple~`. You can `~easily~` `~just~` remove the offending words and the sentence keeps its meaning:

* ❌ Obviously, you can terminate the program at any time by hitting `Ctrl+C`
* ✅ You can terminate the program at any time by hitting `Ctrl+C`

Sometimes, you need to reword to avoid implying that something is simple:

* ❌ It's easy to add new widgets using Acme's tool. Click `menu` -> `add widget`.
* ✅ To add a new widget using Acme's tool, click `menu` -> `add widget`.

## Avoid relying on formatting for emphasis

It's occasionally useful to use **bold** to draw the reader's attention to something, but this should be done very sparingly, and never for whole phrases or sentences at a time. Generally use **bold** or _italics_, but never mix them in the same document, unless there is a well-defined convention of when to use which.

Never use underlining, unless there is a well-defined existing convention about what it means in a specific context.

Rather use word order, sentence structure, and punctuation to draw the reader's attention to important sections where possible.
