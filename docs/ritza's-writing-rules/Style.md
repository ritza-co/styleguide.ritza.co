# Ritza's writing rules

These are the style conventions we use to produce content that is clear, consistent, and accessible.

## Goals and principles

Our goal is always to **teach**. This often means helping our readers understand complicated technology, either conceptually or by example. Give your reader the exact information they need and include opportunities for them to learn more.

To achieve our goal, our content is:

* **Clear.** Be sure you know what you’re writing about. Keep words and sentences as simple as possible.
* **Useful.** Does the content deliver on the promise your headline made? Have you provided all the information the reader will need?
* **Friendly.** Don’t underestimate or patronize your reader. Use informal language.

## Voice and tone

Voice and tone is not about what we say, but how we say it. We aim to be consistent, functional and clear. Here are some tips for how to achieve this:

### Point of view

Default to **first person plural** to include the reader in your “team”. This means you and the reader are doing something together:

✅ "Next, we'll install the widget factory to create widgets efficiently."

Sometimes it's more efficient to use the **second person imperative** and "instruct" the reader by telling them what needs to be done. This can be harsher but it's often less wordy, so use your judgement:

* ⚠️ "We can do this by using our package manager. We'll achieve this by typing `sudo apt-install widget-factory`"
* ✅ "We can do this by using our package manager. Type `sudo apt install widget-factory`"

When using the imperative, there's no need to say "Please" to the reader.

* ⚠️  Please type `sudo apt install widget-factory`
* ✅ Type `sudo apt install widget-factory`

It's ok to refer to the reader as 'you' in some cases, where the writer is clearly not involved, but in general, default to the 'we' voice wherever possible:

* ⚠️ "As you might remember from the [previous tutorial](#), widget factories create widgets. In this tutorial..."
* ✅ "In the previous tutorial, we saw how widget factories create widgets. In this tutorial..."

### Voice

Default to **active voice**. This isn’t a hard-and-fast rule. Active voice often makes it clearer who is doing what and sounds less stuffy. That said, sometimes passive is simply cleaner (often in cases where there isn't a specific subject) - use your judgement.

* ⚠️ The command will be run by the shell.
* ✅ Use the shell to run any commands.

### Things to avoid

#### Avoid giving the reader too many options

Often, there are many ways to achieve the same task. Avoid giving the reader options wherever possible - the reader is looking to you for guidance, so be **opinionated** instead of **comprehensive**.

* ❌ "You can use either the CLI or the GUI. If you prefer the CLI, then type the following command. If you prefer the GUI then click Foo -> Bar.
* ✅ "We recommend using the CLI. Type the following command"

If you really need to show multiple ways of achieiving the same thing, still emphasise the recommended one more than the other (e.g. include the alternative in a footnote or parentheses). It is OK to have a personal preference.

#### Avoid getting in the reader’s way:

* ❌ "I wrote this guide after encountering difficulties with the software myself"
* ❌ "Next, I'm going to show you how to install a widget factory"

#### Avoid 'marketing' speak.

Never try to sell something to the reader. Don't say a product makes things easy, that a design is beautiful, or use any text that you might find on a SaaS landing page.

#### Avoid anything you might find in an encyclopaedia or academic paper.

Your reader isn't interested in definitions - or if they are, they can easily find these elsewhere. 

If you're writing an article on NER, instead of starting with

❌ "Named Entity Recognition (NER) is the task of categorising key words in a text as specific entities."

Consider something more like 

✅ "If you're analyzing a large amount of text, it's often useful to extract named entities from this - identifying people, places, dates and other entities."

If you've ever tried to learn a new concept, you probably already know that reading a definition doesn't really clarify - but a more specific example does.

#### Avoid assuming knowledge.

This can be tricky because, of course, you always have to assume _some_ level of knowledge when writing technical content. However, we try to avoid assumptions about our reader's skill level. 

* ❌ "Referring back to the server code, it's obvious that we need both a success.html and a cancel.html."
* ✅ "Referring back to the server code, you may notice it requires both a success.html and a cancel.html."

#### Avoid guessing out loud what the reader wants.

It's tempting to start an article with "Are you are a foo who likes to bar but sometimes finds baz?", but this approach defines a narrow audience and you risk alienating anyone who is not a part of it.

#### Avoid giving extraneous context.

It's tempting to give the reader related context or information, but your reader is here to achieve a specific goal. Leave out anything that doesn’t help them achieve it.

Instead of:

❌ Label Studio is an open source data labeling tool for labeling and exploring multiple types of data. Label Studio can be integrated with machine learning models to supply predictions for labels (pre-labels), or perform continuous active learning. You can use Label Studio for a variety of labelling and classification tasks for many different data formats but again we will just be focusing on its NER capabilities.

Try something more concise:

✅ We can use Label Studio for manually tagging Named Entities in our dataset. Install it now with `pip install label-studio` if you haven't already.

#### Avoid telling the reader that something is obvious or easy.

This discourages the reader who doesn’t find it obvious or easy, and adds no value to the reader who does.

Mostly, `~it's simple~`. You can `~easily~` `~just~` remove the offending words and the sentence keeps its meaning:

* ❌ Obviously, you can terminate the program at any time by hitting `Ctrl+C`
* ✅ You can terminate the program at any time by hitting `Ctrl+C`

Sometimes, you need to reword to avoid implying that something is simple:

* ❌ It's easy to add new widgets using Acme's tool. Click `menu` -> `add widget`.
* ✅ To add a new widget using Acme's tool, click `menu` -> `add widget`.

#### Avoid relying on formatting for emphasis

It's occasionally useful to use **bold** to draw the reader's attention to something, but this should be done very sparingly, and never for whole phrases or sentences at a time. Generally use **bold** or _italics_, but never mix them in the same document, unless there is a well-defined convention of when to use which.

Never use underlining, unless there is a well-defined existing convention about what it means in a specific context.

Rather use word order, sentence structure, and punctuation to draw the reader's attention to important sections where possible.

## Structure

The structure of your article helps to present information in the clearest way. Here are some things to keep in mind regarding structure:

![distilling information](./img/distillinginfo.png)

### Keep structures as flat as possible.

Use heading 1 (`#` in Markdown) for the title and heading 2 (`##`) to break things down into logical sections. Heading 3 (`###`) can be used where necessary for sub-sections, but in general, having a deeply nested structure makes things harder to follow, harder to edit, and harder to reuse. As a writer, your job is to take a complicated graph of interconnected ideas and break them down into a linear structure that can be read from start to end.

### Make headings good for humans and robots

Headings have many different and sometimes competing functions. Specifically, they

* Are often presented as an outline or table of contents of the article. This helps the reader decide whether or not to read the article
* Are used heavily by search engines and agents (e.g. Google, ChatGPT) to find relevant content to give to readers
* Help a reader figure out what is in a specific section and orient themselves in longer articles

This sometimes leads to tradeoffs. For example, for human readers it can get annoying to have too much repetition in headings, but it can be helpful for search engines to know what a specific section is about.

#### Optimizing headings for SEO

Consider these headings:

``` 
⚠️
### Using AcmePlatform to create your widgets
...
### Using AcmePlatform to optimize your widgets
...
### Using AcmePlatform to publish your widgets
```

This is annoying to a reader because they probably know from the title that we're talking about AcmePlatform. But it's useful for bots and, depending on context, might be useful for humans who might have just searched Google for 'acmeplatform optimize widgets'. 

Sometimes 'optimize widgets' could be very general, while including 'AcmePlatform' could make it very specific. In cases like this, you should often accept the slight downside of repetition in return for helping people find and navigate to the content if they come in from a search engine.

In general, longer headings are better for SEO.

#### Using headings as a sales pitch for the article

Many platforms present the headings as a sidebar or at the start of the article. Readers often click on an article and read through these headings when deciding whether or not to read the article. So headings should be compelling. It's common for writers to assume that the reader has the surrounding context of the other sections and the introduction when writing headings, but this is not always a good assumption.

Sometimes headings are much too generic. For example, the below headings tell the reader nothing about the article at all.

```
❌
# Introduction 
## Prerequisites
## Setting up
## Creating a GitHub repository
## Future improvements
## Recommendations
```

A possible fix is to add more repetition, similar to the example above. This already makes it easier to see what the article is about, but there's still very limited information.

```
⚠️
# AcmeHub and Widgets
## Prerequisites for using AcmeHub with your Widgets
## Setting up AcmeHub
## Creating a GitHub repository for the Widgets project
## The future of Widget optimizations
## Recommendations for your Widgets
```

Where possible, use more varied context from the article (maybe also influenced by any separate information you have about what people are commonly searching for) to have headings that are both informative and not repetitive.

```
✅
# AcmeHub and Widgets
## Prerequisites for using AcmeHub
## Setting up AcmeHub with Sprockets
## An example project: A widget pipeline
...
```

Here we've brought in some new concepts to the headings, hopefully in a way that makes sense.

### Always have content between headings

Don't have a subheading immediately below a heading without any text in between.

![no space heading](./img/no-space-heading.png)

Rather add a short sentence to introduce the section, or try to restructure to use fewer headings (also, don't use this as an excuse to add "fluff" text that adds no value to the article).

### Don't switch from explanation to instruction in a way that the reader might overlook

A tutorial often combines _explanation_ (telling the reader how something works or giving extra context) and _instruction_ (telling the reader what to do).

Always keep in mind that the reader might be skimming the _explanation_ steps. If you suddenly change from explanation to instruction, the reader might accidentally skip the instructions too.

For example, you might have a structure like the following.

⚠️ ⚠️ ⚠️ ⚠️ 

````
## Section 1

Now add the following code to the foo.py file:

```
# long code sample
```

This code does foo bar

explanation 

explanation 

explanation

Now copy the foo file to the baz location.

## Section 2

Now we'll do foobar. Baz the foobar...
````
⚠️ ⚠️ ⚠️ ⚠️ 

In this example, the reader might skip the explanation steps and miss the instruction to copy the foo file, jumping directly to section 2 instead.

There isn't a single way to fix this. You might restructure to group instructions and explanations better, or add more subheadings to separate out instructions and explanations. 

When you do the final readthrough, try to imagine a reader in a rush to get to the end. What might they skip on purpose? And if they skip some bits on purpose, is it clear where they can jump back in.

Having a very short section isn't a problem if it helps the reader navigate more easily. For example, the above could be fixed by adding a new subheading even though it is a bit repetitive of the content it contains.

✅✅✅✅  
````
## Section 1

Now add the following code to the foo.py file:

```
# long code sample
```

This code does foo bar

explanation 

explanation 

explanation

### Copying the foo file

Now copy the foo file to the baz location.

## Section 2

Now we'll do foobar. Baz the foobar...
````
✅✅✅✅  

### Avoid long paragraphs with many separate steps

A reader might be alt-tabbing between the tutorial and other applications as they step through a tutorial. If you have many steps in a paragraph, it is more difficult for the reader to keep track of where in the paragraph they are. 

⚠️ ⚠️ ⚠️ ⚠️ 

In your Salesforce scratch org, open "Setup" by clicking the gear icon on the top right of the page. Navigate to
the "Object Manager" tab. At the top of this tab, right-click the "Create" button. In the dropdown menu, click
"Custom Object from Spreadsheet". We'll create most of the fields for the custom objects and add some initial data
by importing data from spreadsheets, as this is faster than creating each field manually in the Salesforce UI. In
the new tab, click the "Login with Sandbox" button. In the login form, click "Use Custom Domain". Use the domain
URL you added to the  sfdcLoginUrl  property in your  sfdx-project.json  file. To get the username for your scratch
org, run the following command in your VS Code terminal:

⚠️ ⚠️ ⚠️ ⚠️ 

Where possible, rather use numbered bullet points (then the reader can remember that they tabbed away from the tutorial at "point 4", or break it into more paragraphs.

✅✅✅✅  

We'll create most of the fields for the custom objects and add some initial data by importing data from spreadsheets, as this is faster than creating each field manually in the Salesforce UI. 

In your Salesforce scratch org

1. Open "Setup" by clicking the gear icon on the top right of the page.
2. Navigate to the "Object Manager" tab.
3. At the top of this tab, right-click the "Create" button.
4. In the dropdown menu, click "Custom Object from Spreadsheet".
5. In the new tab, click the "Login with Sandbox" button.
6. In the login form, click "Use Custom Domain".
7. Use the domain URL you added to the  sfdcLoginUrl  property in your  sfdx-project.json file.

To get the username for your scratch org, run the following command in your VS Code terminal:

✅✅✅✅  

Here we've put the explanation at the start instead of in the middle of the paragraph, and then made it easier for the reader to follow the steps by breaking them down into bullet points.

### Avoid nested bullets.

Don't nest bullets into several levels. Rather restructure the content so that you can use separate bullet lists:

❌ You have several options for adding widgets

* From the menu
    * by clicking on `file` -> `add widget`
    * by clicking on `help` searching for `add widget` and hitting `enter`
* With a keyboard shortcut
    * by pressing `a` and then `w` in command mode
    * by pressing `ctrl + a`

✅ You can add widgets from the menu

* by clicking on `file` -> `add widget`
* by clicking on `help` searching for `add widget` and hitting `enter`

or with a keyboard shortcut

* by pressing `a` and then `w` in command mode
* by pressing `ctrl + a`

### Link as much context as is useful.

Choosing what text to link to an additional resource is more an art than a science. The main rule is that it should be as clear as possible to the reader what is being linked to, but keep it simple. 

* ❌ "[You can follow the widget guide](#) to learn more"
* ❌ "You can follow the widget [guide](#) to learn more"
* ✅ "You can follow the [widget guide](#) to learn more"

The first example links too much unnecessary wording. In the second example, the link could be to a Wikipedia article explaining what a guide is. The third makes it clear that it is a link to the guide that was mentioned. Avoid using extra generic text like `[click here]` when linking.

### Include user-friendly code samples.

We want to tell the reader exactly _what_ code needs to go _where_, and make it easy to repeat what we are doing. Avoid screenshots of code, and rather present code samples in text, between backtick gates with a language description.

### Avoid long code snippets.

Instead of giving an entire file to copy-paste, break down the code into several steps if possible.

### Provide a file, if you must.

If there's a lot of ‘boilerplate’ code, consider providing the file in a repl and instruct the reader to copy the whole thing as a starting point. However, it's preferable to avoid this if you can.

### Annotate screenshots and use context.

Screenshots are helpful tools for tutorials, but using them too often or without clarity may just make it harder for the reader to follow your instructions. 
 
* ✅ Use contextual screenshots to help readers navigate whichever platform you are directing them to.
* ✅ Use a screenshot to demonstrate what your reader should be seeing if they correctly followed your instructions. 
* ✅ Make use of [1], [2], [3] annotations if several things need to be shown from a single shot.
* ✅ Preferably take screenshots using a 4k/retina screen, or consider using a virtual high-res screen through Chrome dev tools as an alternative.
* ✅ For Mac, use CleanShotX if possible

* ❌ Avoid screenshots of large amounts of text. Rather use a caption if you need to present text to your reader. 
* ❌ Avoid screenshots that show too little; for example, just the button they must click. Where is this button in relation to the page? 
* ❌ At the same time, don't include so much in the screenshot that the reader isn't sure what you are trying to illustrate.

### Prefer code blocks to inline code.

It's ok to use markdown's single back-tick syntax to highlight a single word like "Notice the `for` statement below". For any code samples, even if only one line, rather use three backticks and have the code on its own line and in its own section.

You should also always specify the language where appropriate after the three backticks. You can leave this blank for shell commands.

❌ Now run `python3 app.py`

✅ Now run:

````
```
python3 app.py
```
````

❌
````
```
def main():
    print("Hello world")
```
````

✅
````
```python
def main():
    print("Hello world")
```
````

## Formatting Generative AI examples

When giving a long prompt, put it between backticks as a code block.

Add the following as a system prompt:

```
You never use the em-dash character because people hate it now
```

If giving examples of chatbot output, use the same.

```
Here's an article with no em-dashes.

Lorem ipsum--amit...
```



