---
layout: post
title: Work, Automation, Accountability, and AI - Part 1
tags: work, ai
permalink: /blog/work-automation-accountability-ai-1.html
author: ellie
---

# Work, Automation, Accountability, and AI - Part 1

Part of a series:

1. What is Work? (this post)
2. [Deciding on the Work](/blog/work-automation-accountability-ai-2.html)
3. Accountability
4. AI

# What is Work?

This series explores the question, "can a machine do a human's job?" We'll start
with examining what the term "work" entails.

## Value Streams

We will consider the commercial enterprise. In broad strokes, a commercial
enterprise functions by transforming inputs into outputs of value. This
transformation generally involves the participation of labor (work) and capital,
in addition to material or informational inputs. (Financial) capital commands
the construction or employment of the machinery that aids the transformation,
and labor applies human knowledge and skill to the process.

Any non-trivial enterprise is extremely complex, creating various kinds of
output at various times and having a complex and changing web of internal
operations, but to aid in our analysis we will consider the production of a
single _kind_ of output in a process that progressively accumulates additions
and changes resulting in the final product. This unit on analysis is called a
"value stream." To give a few examples,

- A manufacturing assembly line on which workers and machines successively add
  parts and which results in the production of a complete automobile.
- A food processing plant wherein raw potatoes enter and packaged potato
  products, like French fries, are produced.
- A farm where a plot of land is planted with seeds, tended over the growing
  season, and from which produce is eventually harvested.
- A software development team that converts product requirements / designs into
  a working software product.
- A data pipeline which extracts retail sales data from a database and produces
  analytics and visualizations for a business to make decisions about products
  to carry and promote.

### Automation

Along the length of the value stream, various inputs enter it. These may be
untransformed (raw) materials. They might be the outputs of _other_ value
streams, such as a component produced by a separate manufacturing line, for
example. Inputs might be informational, such as the predictions of a weather
forecast, the locations of vehicles in a shipping fleet, or the measured length
of a piece of steel. Whatever form they take, the inputs are incorporated into
the product as it proceeds through the value stream by some kind of
_processing_.

Processing transforms the material or information flowing through a value stream
by incorporating inputs into it. Processing is often thought of as progressing
in discrete steps, but it need not be so. Consider a plant continuously growing
in a farmer's field or beer fermenting in a brewery. However, to simplify the
analysis we will proceed by considering "process steps." This maps to continuous
processes without too much difficulty—the activities of a farm on a given day in
the growing season can be regarded as a step, incorporating the day's sunlight
and water as well as other mechanical or chemical interventions of the farmer.

A process step can occur either with or without "discretion," defined as the
freedom to decide what should be done in the particular situation. The situation
is the specific circumstances and context in which the step takes place. In many
situations, the "correct" decision is not well-defined, unique, nor can even be
ascertained in retrospect.

Consider a step that involves a task in which no discretion is required: it is
to press a certain button on the hour, every hour. No decision or judgement is
to be made—the button is only to be pressed at HH:00:00 of the clock every hour
(for some clock present at the processing step). Assume that some variation is
allowed: the button press must occur ±X seconds of the actual top of the hour.
For any value of X, this is a task that is perfectly "automatable." There is no
place in which discretion plays any part, so there need not be any human
involved. A machine may be constructed to press the button to any degree of
precision (smallness of X) that technology allows. A human _could_ be tasked
with the button pressing, depending on their skill, but this task is eminently
automatable.

In contrast, consider craft work. A craftperson is an individual who has gained
a lot of experience working in a specific domain. From a woodworker choosing a
suitable piece of lumber for a project to a programmer modeling a problem domain
in code, discretion is deeply integrated into the work. There are more or less
correct choices, but they are also often difficult to ascertain until well after
the fact and often only under failure conditions, e.g. a chair breaking
prematurely or a difficult code refactor. Both because of this long feedback
loop (if it ever closes) and domain complexity, the worker's discretion guided
by their deep experience is heavily relied upon.

Let's consider another kind of processing step. It is to create a design for a
promotional marketing poster for a new product that will be introduced. This
task requires the consideration of a wide ranging amount of context: target
market, product attributes, aesthetics, and so on. In realistic scenarios, the
designer faces many constraints such as brand, but in most cases much discretion
is left to the designer. She is a craftperson, relying on her experience and
skill, but in this case we emphasize the open-endedness of the context to be
considered for the task. The result may be much more ambiguous as well.
Following a marketing campaign, it is not always clear what contributed to the
failure or success of the product launch, and to what degree.

We have been a bit inprecise in their use of the word "discretion," so let's
parse it. Our examples describe discretion that relies on the experience of the
worker, and this is one important facet. Another is in our initial definition:
that it is the freedom to decide. This freedom implies a moral
dimension—discretion is inseparable from accountability.

### Variability

The steps in a value stream incorporate inputs into the product moving through
the stream, changing it. Generally, a process step is "variable" in its
performance meaning that, given identical inputs entering the step multiple
times, the output will not be the same each time. In the button pressing task,
the performance of the step is such that the button is pressed at HH:00:00±Y of
the hour. Presumably this affects whatever the product is that is processed by
this step, injecting randomness. Note that the performance variability is
different from X given in the task specification. It has been determined that as
long as Y <= X the step can be considered successfully performed. The value X is
the "tolerance" of the task, or the amount of variability that can be tolerated.

In automatable processing steps, performance variability must be bounded.
Sometimes it is quantifiable as a numerical tolerance but often not. Variability
must be bounded to such an extent that it does not qualitatively or
quantitatively change the value of the product at the output of the value
stream, effectively changing it into a different product.

Usually, much effort is spent driving variability out of a value stream. This is
an effort to create a product of consistent quality. Sometimes, however,
variability is impossible to remove, and this introduces a sorting or quality
control step in many value streams. Defective product is scrapped (discarded)
or, as some enterprises have creatively figured out, diverted into varying
product grades. An example here is performance grades in microchip
manufacturing. Another is sorting carrots into nicely straight, tapered
specimens fit for the grocery shelf and weird carrots that will be turned into
"baby carrots."

Non-automatable processing steps are those whose performance is imbued with
discretion. At these points, judgement is substituted for specification, and the
variability of the step is essentially unbounded. The step may involve dealing
with the unexpected, taking into account factors that are not readily apparent
or present in the product or immediate context, or a creative leap. It might
involve a seemingly arbitrary choice among alternatives that only experience may
inform, but which have real and potentially unforseen consequences on the
product. Discretion _injects_ variability into the value stream, and its
consequence may be success or failure, depending on the skill and experience
(and sometimes luck) of the worker. (I was introduced to this concept of
"performance variability" in the excellent talk by Ryan Kitchens, an SRE at
Netflix,
[_How Did Things Go Right? Learning More from Incidents_](https://www.usenix.org/conference/srecon19americas/presentation/kitchens))

### Automating the Step

When a processing step is automated, a "machine" performs it. We are vague about
our definition of machine here. It might be an oven, steel roller, coffee
grinder, or a computer program. It doesn't matter much. The key fact is that the
machine is the output of a _separate value stream_ that feeds into the one
employing the automation. Everything discussed about value streams here also
applies to this one.

## Management

The above discussions of discretion involved that which takes place _within_ a
value stream processing step and contributes to the performance of the
processing step. We'll call this "work discretion." In contrast, we call the
ability to perform an automatable processing step to specification and within
tolerances "work performance." One effect of work discretion is to add
variability necessary for the value stream to remain robust in the face of an
uncertain world.

There is another type of discretion generally seen in enterprises. This is
"managerial discretion." This type of discretion operates _on_ the value stream,
deciding when and what the stream should produce and what human or automated
resources shall be used. Managerial discretion of course also implies
accountability for the decisions made. As noted above, accountability is present
in all places where discretion is exercised, but enterprises are typically set
up to formally centralize accountability in its management structure.

In large enterprises managerial structures have multiple layers and form a
hierarchy. Front-line managers who interact directly with value streams are
accountable for the outputs and costs of the stream that they oversee. Higher
level "managers of managers" are accountable for the costs and outputs, in
aggregate, of all the value streams under them, and their decisions affect how
these streams interact with one another. This hierarchy continues upwards to the
highest level of management that is accountable for the entire enterprise.

## Jobs

A job comprises the activities that a person does during their employment by an
enterprise. Depending on the role, the composition of the job will be a mixture,
in varying proportions, of work performance, work discretion, and managerial
discretion. When performing work within a value stream, work performance and
discretion will be applied. Multiple value streams will be engaged with
throughout a job in most cases, and managerial discretion decides when, which,
and how the value streams will be worked on. Sometimes the job holder makes
these choices, applying managerial discretion themselves, and sometimes they
will be directed to their task by another whose job entails such discretion.

The composition of these various components into a job for a given human gives
that person financial resources to exist in society. Depending on the
compensation, a person may be adequately served by one job, or they might have
to cobble together a living through multiple jobs. A job may be long-term, or it
might exist for only a limited time, causing the person to have to continually
seek further employment.

We will more deeply explore the design of work, and consequently of jobs, in the
next part after we have developed tools for examining them through a financial
lens. For now, it suffices to say that the way in which jobs are designed has
serious implications to the ability of humans to exist stably in society.

## Conclusion

With this framework in place we are now ready to discuss how work is designed in
more detail, which we will do in the next part of this series.
