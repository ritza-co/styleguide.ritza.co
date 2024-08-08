# Structure

The structure of your article helps to present information in the clearest way. Here are some things to keep in mind regarding structure:

## Keep structures as flat as possible.

Use heading 1 (`#` in Markdown) for the title and heading 2 (`##`) to break things down into logical sections. Heading 3 (`###`) can be used where necessary for sub-sections, but in general, having a deeply nested structure makes things harder to follow, harder to edit, and harder to reuse. As a writer, your job is to take a complicated graph of interconnected ideas and break them down into a linear structure that can be read from start to end.

![distilling information](./img/distillinginfo.png)

## Always have content between headings

Don't have a subheading immediately below a heading without any text in between.

![no space heading](./img/no-space-heading.png)

Rather add a short sentence to introduce the section, or try to restructure to use fewer headings (also, don't use this as an excuse to add "fluff" text that adds no value to the article).

## Don't switch from explanation to instruction in a way that the reader might overlook

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

## Link as much context as is useful.

Choosing what text to link to an additional resource is more an art than a science. The main rule is that it should be as clear as possible to the reader what is being linked to, but keep it simple. 

* ❌ "[You can follow the widget guide](#) to learn more"
* ❌ "You can follow the widget [guide](#) to learn more"
* ✅ "You can follow the [widget guide](#) to learn more"

The first example links too much unnecessary wording. In the second example, the link could be to a Wikipedia article explaining what a guide is. The third makes it clear that it is a link to the guide that was mentioned. Avoid using extra generic text like `[click here]` when linking.

## Include user-friendly code samples.

We want to tell the reader exactly _what_ code needs to go _where_, and make it easy to repeat what we are doing. Avoid screenshots of code, and rather present code samples in text, between backtick gates with a language description.

## Provide a file, if you must.

If there's a lot of ‘boilerplate’ code, consider providing the file in a repl and instruct the reader to copy the whole thing as a starting point. However, it's preferable to avoid this if you can.

## Annotate screenshots and use context.

Screenshots are helpful tools for tutorials, but using them too often or without clarity may just make it harder for the reader to follow your instructions. 
 
* ✅ Use contextual screenshots to help readers navigate whichever platform you are directing them to.
* ✅ Use a screenshot to demonstrate what your reader should be seeing if they correctly followed your instructions. 
* ✅ Make use of [1], [2], [3] annotations if several things need to be shown from a single shot.
* ✅ Preferably take screenshots using a 4k/retina screen, or consider using a virtual high-res screen through Chrome dev tools as an alternative.
* ✅ For Mac, use CleanShotX if possible

* ❌ Avoid screenshots of large amounts of text. Rather use a caption if you need to present text to your reader. 
* ❌ Avoid screenshots that show too little; for example, just the button they must click. Where is this button in relation to the page? 
* ❌ At the same time, don't include so much in the screenshot that the reader isn't sure what you are trying to illustrate.

## Prefer code blocks to inline code.

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
