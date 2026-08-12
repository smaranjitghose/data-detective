## A record and an answer are not the same thing

Open the screen time settings on your phone. You will find two things on the same page.

One is a record: every app you opened, and how long you stayed in each, hour by hour. The other is a sentence, something like *your daily average is up from last week*. Both come from the same source. Only one of them tells you anything you might act on.

Go and look at yours before reading further. The record and the sentence sitting side by side is the whole idea of this topic, and you have been carrying it in your pocket.

## A file of penguins, and one question

Between 2007 and 2009, researchers at Palmer Station in Antarctica caught penguins, measured them, and wrote the measurements down. Here are the first five rows of what they recorded:

| species | island | bill_length_mm | bill_depth_mm | flipper_length_mm | body_mass_g | sex |
| ------- | --------- | -------------: | ------------: | -----------------: | -----------: | ------ |
| Adelie | Torgersen | 39.1 | 18.7 | 181 | 3750 | male |
| Adelie | Torgersen | 39.5 | 17.4 | 186 | 3800 | female |
| Adelie | Torgersen | 40.3 | 18.0 | 195 | 3250 | female |
| Adelie | Torgersen | NA | NA | NA | NA | NA |
| Adelie | Torgersen | 36.7 | 19.3 | 193 | 3450 | female |

There are 344 rows in total, covering three species on three islands. The file is free to download and you will use it repeatedly later in the course.

Now the question the researchers cared about: do the three species differ in size?

Read the table again and notice that it does not answer this. Not because the table is poor, but because an answer of that kind is never sitting in a row. It appears only when you take one column, split it by species, and compare the groups. Do that with flipper length and a clear result comes out: Gentoo penguins have much longer flippers than Adelie and Chinstrap penguins.

> A record plus a question plus a comparison gives you an answer. Data is the record. Information is the answer.

## What counts as data

Data is anything someone wrote down about what happened or what was measured.

That net is wider than most beginners expect. All of these are data:

* a temperature reading logged by a sensor every minute
* a row in an order system holding a product, a quantity, and a date
* a customer message saying the package arrived damaged
* a photograph of a water meter

Numbers are not the requirement. Being recorded is the requirement.

There is a limit to this, and it catches people out. A fact you know but nobody wrote down is not data. A field researcher who notices that one penguin looks unusually large knows something real, and if it never reaches a column, no analysis will ever see it. A large share of what goes wrong in data work comes from this gap between what happened and what got recorded.

## What a single row has to carry

Look at any row of the penguin table and you can name four things it holds. Together they are what makes a row usable rather than decorative.

| Part of a row | In the penguin file | What goes wrong without it |
| ------------------- | ---------------------------- | --------------------------------------------- |
| What is being described | One penguin | You cannot tell whether two rows are the same bird |
| Which property | Flipper length, body mass, sex | The number has no meaning |
| The value | 181, 3750, female | Nothing to compare |
| The unit or scale | Millimetres, grams | 181 could be centimetres, and the comparison breaks |

The unit row is the one people skip. A file recording bill length in millimetres and another recording it in centimetres will merge without complaint and produce a group of penguins ten times larger than the rest. Nothing in either file objects, because both columns are numbers and both are called `bill_length`.

## The same file, three different questions

Information is not a better grade of data, and it is not what you get by processing data harder. It is what appears when you bring a question. The file is identical in all three rows below:

| The question | What you compare | The answer that comes out |
| ------------------------------------- | -------------------------------- | ---------------------------------------------- |
| Do the species differ in size? | Flipper length, split by species | Gentoos are much larger than the other two |
| Are the islands equally studied? | Row counts, split by island | Coverage is very uneven across the three |
| Are males and females both represented? | Row counts, split by sex | Some rows have no sex recorded at all |

Nothing in the file changed between those rows. The question changed, then the comparison, then the answer.

## The shape it arrives in, and who produced it

Two practical things to establish about any file before you work with it.

The first is its shape, which decides how much work happens before you can ask anything.

| Shape | What it looks like | What it costs you first |
| --------------- | ----------------------------------------------- | ---------------------------------------- |
| Structured | Fixed columns, one row per thing, like the penguin table | Almost nothing, start looking |
| Semi-structured | Field names travel with each record, records can differ | Reshaping it into a table |
| Unstructured | No fields at all: emails, photos, audio | Extracting something countable, a project in itself |

The second is who produced it and why. The penguin measurements were primary data for the research team, who chose what to measure and how. For you they are secondary data: collected by someone else, for their purpose, with decisions already baked in that you cannot see. Census tables, World Bank figures, and anything downloaded from data.gov.in are the same.

Six questions cover most of what you need to know about a file you did not collect:

| Question | Why it matters |
| ---------------------------- | ----------------------------------------------- |
| Who recorded it? | Whose interests shaped what got written down |
| Why was it recorded? | The original purpose may not match yours |
| When was it recorded? | The situation it describes may have changed |
| How was it recorded? | Method decides what could be captured at all |
| Who or what does it cover? | Defines who falls outside the file entirely |
| What does each field mean? | Prevents confident misreading |

That last one gets skipped because column names look obvious. The penguin file has a `year` column. Does it hold the year the bird was measured, the year the study season began, or the year the record was typed up? The number looks identical in all three cases and the analysis is not.

## Before you trust a number

Look at the fourth row of the table again. Every measurement is missing. Eleven other rows in the file have no sex recorded. Count penguins by sex and your total comes out below 344, with nothing on screen explaining the shortfall.

Missing values are the easy version of this problem, because you can see them. The hard version leaves no trace. Suppose an online store's ratings are 95% five-star. Customers may be delighted. Or unhappy customers may not bother rating. Or the system may only request a rating after a successful delivery, so the unhappy ones are never asked.

The numbers look identical in all three cases, and no further calculation on those numbers will separate them. Only knowing how the ratings were collected will.

## Check yourself, then open a file

| Statement | Data or information? | Why |
| ------------------------------------------- | ----------- | -------------------------------------------- |
| `flipper_length_mm = 181` | Data | One recorded measurement, no question attached |
| Gentoos have longer flippers than Adelies | Information | A comparison across groups answering a question |
| A folder of 4,000 customer emails | Data | Recorded, unstructured, not yet answering anything |
| 95% of ratings are five stars | Information | A count turned into a proportion |

Notice the last row. Information can be produced correctly and still mislead, which is why the question of how the data was collected never goes away.

When you next meet a new file, spend ten minutes on three things: read twenty rows slowly, write down one question you would want answered, and list what you think is missing from the file. That is not preparation for the work. It is the beginning of it.
