# [An Elegant Puzzle: Systems of Engineering Management](https://www.goodreads.com/book/show/45303387-an-elegant-puzzle)

## Introduction

Organisational design gets the right people in the right places, empowers them to make decisions, and then holds them accountable for their results.

## Organisations

An organisation is a collection of people working toward a shared goal.

Organisational design is the attempt ot understand why some create such energy and others create mostly heat: friction, frustration, and politics.

### Sizing teams

The fundamental challenge of organisational design is sizing teams.

**Managers should support six to eight engineers.** This gives them enough time for active coaching, coordinating, and furthering their team's mission by writing strategies, leading change and so on.
  * Fewer than four engineers tend to function as **Tech Lead Managers**, taking on a share of design and implementation work.
  * Managers supporting more than eight or nine engineers act as **coaches** and safety nets for problems.

**Managers-of-managers should support four to six managers.** This gives them enough time to coach, align with stakeholders, and to do a reasonable amount of investment in their organisation.
  * Managers supporting fewer than four other managers should be in a period of active learning.
  * Supporting a large team of managers leaves you functioning purely as a problem-solving coach.

**On-call rotations want eight engineers.** It is sometimes necessary to pool multiple teams together to reach the eight engineers necessary for a 24/7 on-call rotation.

**Small teams (< 4 members) are not teams.** Fewer than four individuals are sufficiently leaky abstraction that they function indistinguishably from individuals.  A few tips:
* Teams should be six to eight during steady state.
* To create a new team, grow an existing team to eight to ten, and then bud into two teams of four or five.
* Never create empty teams.
* Never leave managers supporting more than eight individuals.

### Staying on the path to high-performing teams

Four stages of a team

* **A team is falling behind** if each week their backlog is longer than it was the week before. To fix this, hire new people and increase capacity.
* **A team is treading water** if they're able to get their critical work done, but are not able to paying down technical debt or begin major new projects. To fix this, consolidate team efforts to finish more things, and reduce concurrent work until able to begin repaying debt.
* **A team is repaying debt** when they're able to start paying down tech debt, and are beginning to benefit from the debt repayment snowball. To fix this, add time to pay debt.
* **A team is innovating** when their technical debt is sustainably low, morale is high, and the majority of work is satisfying new user needs. To fix this maintain enough slack in your team's schedule so that the team can build quality into their work.

For each constraint, prioritise one team at a time, this is particularly important for hiring.

Adding new individuals to a team disrupt the team. It is much easier to have rapid growth periods for any given team, followed by consolidation/gelling periods.

### A case against top-down global optimisation

#### Team first

Sustained productivity comes from high-performing teams, be hesitant to disassemble them.

A proposed model is to rapidly hiring into teams loaded down by technical debt, not into innovating teams, which avoids incurring re-gelling costs on high-performing teams.


#### Fixed costs

Moving one person can shift an innovating team back into falling behind.

#### Slack

Don't add more resources to a team with visible slack, inverse does not apply.

In defence of having slack, teams put spare capacity to great use by improving areas within their aegis, in bot incremental and novel ways.

#### Shift scope; rotate

It's more fruitful to move scope between teams. If a team has significant slack, then incrementally move responsibility to them.

Another approach is to rotate individuals for a fixed period into an area that needs help.

### Productivity in the age of hypergrowth

#### More engineers, more problems

Integrating large numbers of engineers is hard. The challenge depends on how quickly you can ramp engineers up ot self-sufficient productivity. You can quickly find a scenario in which untrained engineers increasingly outnumber the trained ones.

It is not just training and hiring tho:
1. For every additional order of magnitude of engineers, you need to design and maintain a new layer of management.
2. For every ~10 engineers, you need an additional team and more coordination.
3. You'll need to improve your development tools
4. More deployments drive more outages.
5. Relative time invested in on-call goes up.

At high enough rates, the marginal added value of hiring gets very slow, especially if your training process is weak.

#### Systems survive one magnitude of growth

If your company is designing systems to last one order of magnitude and doubling every six months, then you'll have to re-implement every system twice every three years.

The real productivity killer is not the system rewrites, but the migrations that follow up those rewrites.

#### Ways to manage entropy

You only get value from projects when they finish. When your company has decided that is going to grow you cannot stop it from growing. However, you absolutely can concentrate that growth, such that your teams alternate between periods of rapid hiring and periods of consolidation and gelling.

Companies do major investments in both new-hire bootcamps and recurring educational classes.

If you could get training down to four weeks, imagine how quickly you could hire without overwhelming the existing team!

Create a rotation for people who are available to answer questions, and train your team not to answer other forms of interruptions. It may be useful to define an _ownership registry_ and document who owns what.

The best solution to frequent interruptions is a culture of documentation, optimised for reading and searching.

The most important opportunity is designing your software to be flexible. If you are going to rewrite your systems every few years due to increased scale, let's avoid any unnecessary rewrites.

An anti-pattern is the gatekeeper pattern. Having people who perform gatekeeping activities create very odd social dynamics, build systems with sufficient isolation so when they occasionally fail, make sure that they fail with a limited blast radius.

---

As a closing though, the way you handle urgent project requests when you're already underwater is by learning to say no.

### Where to stash your organisation risk?

The idea of _organisational debt_ is sibling of _technical debt_, for example a toxic culture, struggling leader, etc.

These problems bubble up from your peers, skip-level one-on-ones, and organisational health surveys.

Identify a few areas to improve, ensure you're making progress on those, and give yourself permission to do the rest poorly.

It's best to only delegate solvable risk. If something isn't likely to end well, hold the bag yourself, you're almost certainly the best positioned to take responsibility.

### Succession planning

Succession planning is thinking through how the organisation would function without you.

First, figure out what you do:
* Look at your calendar and write down **your role in meetings**.
* Take a pass on you calendar for non-meeting stuff.
* Look out for **recurring processes**, like roadmap, planning, performance calibrations, etc. and document your role in each of those processes.
* For each of the **individuals you support**, in which areas are your skills and actions most complementary to theirs?
* Audit inbound chats and emails for requests and questions coming your way.
* Look at the categories of the work you've completed over the past six months.
* Think on the **external relationships** that have been important for your current role.

For each item try to identify individuals who could readily take on that work. If you cannot find someone, identify a handful of individuals who could potentially take over.

Filter the gaps down to two lists:
1. _Easiest gaps to close_, It may require a written document or quick introduction.
2. _Riskiest gaps_, areas where you're uniquely valuable to the company.

Write up a plan to close all of the easy gaps and _onw or two_ the riskiest gaps. This is a great exercise to run once a year to identify things you could be delegating.

## Tools

The key tools for leading efficient change are systems thinking, metrics and vision/

### Introduction to systems thinking

You should read about [_Thinking in Systems: a Primer_](https://www.goodreads.com/book/show/3828902-thinking-in-systems) by Donella H. Meadows.

Systems thinking makes the observation that links between events are often more subtle than they appear.

#### Developer velocity

Recommended reading [_Accelerate: The Science of Lean Software and DevOps_](https://www.goodreads.com/book/show/39211555-accelerate) by Nicole Forsgren, Gene Kim, and Jez Humble.

To measure developer velocity:
* **Delivery lead time**, time from the creation of code to its use in production
* **Deployment frequency**
* **Change fail rate**, how frequent changes fail
* **Time to restore service**, time spent recovering from defects

Any difficult problem is worth trying to represent as a system. There are a few tools that can help you out: Stella and Insight Maker.

#### Product management: exploration, selection, validation

Many engineering organisations separate engineering and product leadership into distinct roles. This is ideal because they thrive in different perspectives and priorities.

As an engineering leader, you may have to cover both roles temporarily.

Product management is an iterative elimination tournament.
1. **Problem discovery.** Exploring the different problems that you could pick to solve. You populate the problem space based on:
    * **Users' pain**, problems that your users experience
    * **Users' purpose**, what motivates your users to engage with your systems
    * **Benchmark**, how your company compares to competitors. Areas in which you are weak, _consider_ investing in
    * **Cohorts**, what is hiding behind your clean distributions
    * **Competitive advantages**, areas where you're exceptionally strong
    * **Competitive moats**, extreme version of a competitive advantage. Allows you to pursue offerings that others simply cannot
    * **Compounding leverage**, blocks you could start building today that would compound into major product or technical leverage over time.
2. **Problem selection**, narrow down to a specific problem portfolio
    * **Surviving round**, what do you need to survive current round
    * **Surviving the next round**, where do you need to be when the next round in order to avoid getting eliminated?
    * **Winning rounds**
    * **Consider different time frames.** Assumptions about the correct time frame to optimise for
    * **Industry trends**, where do you think the industry is moving
    * **Return on investment**, try ordering problems by expected return on investment
    * **Experiments to learn**
3. **Solution validation**, it's easy to jump directly into execution, but it's well worth to have an explicit solution validation phase.
    * **Write a customer letter**, useful to test against actual users
    * **Identify prior art**, it's better to rely on people you have some connection to instead of on conference talks, there is lot of misinformation out there.
    * **Find reference users**
    * **Prefer experimentation over analysis**, get good at cheap validation
    * **Find the path more quickly travelled**, try to find the cheapest way to validate
    * **Justify switching costs**, the cost of switching for users to move to your solution

#### Vision and strategies

When jumping from supporting managers and supporting their managers alignment may be difficult to handle. Agreeing on strategy and vision is the most effective approach for alignment at scale.

_Strategies_ are grounded documents which explain trade-offs and actions that will be taken to address as specific challenge.

_Visions_ are aspirational documents that enable individuals who don't work closely together to make decisions that fit together cleanly.

##### Strategy

Specific actions that address a given challenge's constraints. Recommended reading [_Good strategy / Bad Strategy: The difference and why it matters_](https://www.goodreads.com/book/show/11721966-good-strategy-bad-strategy) by Richard Rumelt.

The _diagnosis_ is a theory describing the challenge at hand. Before you've even finished reading a great diagnosis, you'll often have identified several good candidate approaches.

The second step is to identify _policies_ that you will apply to address the challenge. Describe the general approach that you'll take, and are often trade-offs between two competing goals.

When you apply your guiding policies to your diagnosis, you get your _actions_. This is the easiest part to write, however publishing it and following through with it can be significant test of your commitment.

Because strategies are specific to a given problem, it's okay to write a few of them. The act of writing a strategy leads folks through a systematic analysis.

##### Vision

If strategies describe the harsh trade-offs necessary to overcome a particular challenge, then _visions_ describe a future in which those trade-offs are no longer mutually exclusive. **An effective vision helps folks think beyond the constraints of their local maxima**, and lightly aligns progress without requiring tight centralised coordination.

Visions should be detailed, but the details are used to illustrate the dream vividly, not prescriptively constraint with its possibilities. Good visions are composed of:
* **Vision statement**, a one or two sentence aspirational statement to summarise the rest of the document.
* **Value proposition**, how will you be valuable to your users and your company?
* **Capabilities**, what capabilities will the product, platform, or team need in order to deliver on your value proposition?
* **Solved constraints**, constraints that you're limited by today, but that in future you'll no longer be constrained by?
* **Future constraints**, constraints that you expect to encounter in this wonderful future?
* **Reference materials**, link to all resources for those who want to understand more of the thinking that went into the vision.
* **Narrative**, synthesise all those details into a short, maybe one page, narrative that serves as an easy-to-digest summary.

**A vision is succeeding when people reference the document to make their own decisions.**

Some additional tips:
* **Test the document** sit down with a few different folks to get their perspectives and iterate.
* **Refresh periodically**
* **Write simply** You'll likely want _one vision for every complete distinct area, but no more_.

#### Metrics and baselines

Goals decouple the "what" from the "how"

Goals are a composition of
1. A **target** states where you want to reach
2. A **baseline** identifies where you are today
3. A **trend** describes the current velocity
4. A **time frame** sets bounds for the change

Two interesting kinds of goals: investments and baselines. Investments describe a future state that you want to reach, and baselines describe aspects of the present that you want to preserve.

The best way to avoid unintended outcomes is to pair your investments goals with baseline metrics (countervailing metrics). 

The most common way to use goals is during s planning process. You'll probably want to identify more baseline goals than investment goals.

OKRs are useful, lightweight structure to start from.

#### Guiding broad organisational change with metrics

Metrics are an extremely effective way to lead change with little or no organisational authority.

1. **Explore**: The first step is to get data in an explorable format in your data warehouse.
2. **Dive**: Go deep on understanding the levers.
3. **Attribute**: Diving will uncover one team who are nominally accountable for the metric's performance.
4. **Contextualise**: Start to build context around each team's performance by doing benchmarking against a small handful of cohorts like backend, frontend or infrastructure.
5. **Nudge**: Nudge them for action! Send push notifications, typically email, to teams whose metric has changed recently, both in terms of absolute change and in terms of their benchmarked performance against their cohort. Recommended read [Nudge](https://www.goodreads.com/book/show/2527900.Nudge).
6. **Baseline** some cases contextualised nudges are not enough, you may need to agree on the baseline metrics for performance.
7. **Review** hopefully you won't need to reach, is running a monthly or quarterly review that looks each team's performance.

#### Migrations: the sole scalable fix to tech debt

Migrations matter because they are usually the only available avenue to make meaningful progress on technical debt.

Each migration aims to create technical leverage. Moving from VMs to containers, rolling out circuit-breaking, moving to the new build tool… If you don't get effective at software and system migrations, you'll end up languishing in technical debt.

##### De-risk

Write a **design document** and shop it with the teams that you believe will have the hardest time migrating. Test it against the next six to twelve months of the roadmap and iterate.

**Embed into the most challenging one or two teams**, and work side by side with them to build, evolve, and migrate to the new system.

**Each team who endorses a migration is making a bet on you**.

##### Enable

It's better to slow down and build tooling to programmatically migrate the easy 90 percent, it reduces the cost radically.

Figure out the **self-service tooling and documentation** that youc an provide to allow teams to make the necessary changes without getting stuck. The best migration tools are incremental and reversible.

Documentation and self-service tooling are products, and they thrive under the same regime.

##### Finish

The last phase of a migration is deprecating the legacy system that you've replaced. It requires 100 percent adoption.

Start by **stopping the bleeding**, which is ensuring that all newly written code uses the new approach.

Start **generating tracking tickets**, and set in place a mechanism which **pushes migration status** to teams.

**Finish it yourself**.

It is important to celebrate migrations, **recognition should be reserved for their successful completion**.

#### Running an engineering reorg

There are two managerial skills that have a disproportionate impact in your organisation success: making technical migrations cheap, and running clean reorganisations.

Checklist to ensure a reorganisation is appropriate:
1. Is there a structural problem? With a reorg you can increase communication, reduce decision friction, and focus attention
2. Are you reorganising around a broken relationship? You'll be better of addressing the underlying issue.
3. Does the problem already exist? It's better to wait until a problem actively exists before solving it.
4. Are the conditions temporary? It may be easier to patch through and rethink on the other side.

##### Project head count a year out

You can design an organisation determining it approximate total size:
1. An optimistic number based on what's barely possible
2. A number based on the "natural size", if every team and role was fully staffed
3. A realistic number based on historical hiring rates.

Merge those into a single number.

##### Manager-to-engineer ratio

Now you need to identify how many individuals you want each manager to support. **If engineering managers are expected to do hands-on technical work, it should be 3 to 5 engineers.**

**Otherwise, 5 to 8 depending on the experience level.**

##### Defining teams and groups

Example: 35 engineers, 7 engineers per manager = you need 5 managers, and 1.8 managers of managers. This is 5 to 6 teams, and maybe one to three groups.

You should generally round up the number of managers.

Few extra considerations:
1. Can you write a crisp mission statement for each team?
2. Would you personally be excited to be a member of each of the teams, as well as the manager of each of those teams?
3. Put teams that work together, as close together as possible.
4. Can you define clear interfaces for each team?
5. Can you list the areas of ownership for each team?
6. Avoid implicitly creating holes of ownership, define understaffed teams.
7. Are you over-optimising on individuals versus establishing a sensible structure?

##### Staffing the teams and groups

Four sources of candidates to staff them:
1. Team members who are ready to fill the roles now
2. Team members who can grow into the roles in the time frame
3. Internal transfers from within your company
4. External hires who already have the skills

##### Commit to moving forward

1. Are the changes meaningful net positive?
2. Will the new structure last at least six months?
3. What problems did you discover during design?
4. What will trigger the reorg _after_ this one?
5. Who is going to be impacted most?

**Organisational change is resistant to rollback, you have to be collectively committed to moving forward with it, even if runs into challenges along the way.**

##### Roll out the change

Key elements to a good rollout:
1. Explanation of reasoning driving the reorganisation
2. Documentation of how each person and team will be impacted
3. Availability and empathy to help bleed off frustration from impacted individuals

Tactics for doing this:
1. Discuss with impacted individuals first
2. Ensure that managers are prepared to explain the reasoning behind the changes
3. Send an email out documenting the changes
4. Be available for discussion
5. If necessary, hold an all-hands by try not to (people don't process well in large groups)
6. Double down on doing skip-level one-on-ones

#### Identify your controls

When you partner with managers it may be difficult to remain effective without understanding their day-to-day tasks.

Controls are the mechanisms that you use to align with other leaders you work with.

**Metrics** align on outcomes while leaving flexibility around how the outcomes are achieved.

**Visions** ensure that you agree on long-term direction.

**Strategies** confirm you have a shared understanding of the current constraints.

**Organisation design** allows you to coordinate the evolution of a wider organisation.

**Head count and transfers** are the ultimate form of prioritisation.

**Roadmaps** align on problem selection and solution validation.

**Performance reviews** coordinate culture and recognition.

Start with this list but don't stick to it!

You will need to agree on the _degree of alignment_ for each one.

**I'll do it**. Stuff that you'll personally be responsible for doing.

**Preview**. You'd like to be involved early and often.

**Review**. You'd like to weigh in before it gets published.

**Notes**. Projects you'd like to follow but don't have much to add to.

**No surprises**. The work that we're currently aligned on but requires updates to keep your mental model in tact.

**Let me know**. If something comes up that you can help with, but otherwise you are totally confident it'll go well.

#### Career narratives

You as a manager, can simply give folks a career path.

##### Artificial competition

Climbing the career ladder has the side effect of funneling most folks toward a constrained pool of opportunity.

An important part of setting your goals is developing areas you're less experienced in to maximise your global success, but it's equally important to succeed locally within your current environment by prioritising doing what you do well.

##### Translating goals

Once you've identified goals to pursue, the next step is to translate those goals into actions, your manager can be a leveraged partner finding the intersection of your interests and the business priorities.

Bringing your list of goals to this discussion helps ensure that it's successful.

#### The briefest of media trainings

Three rules for speaking with the media:
1. **Answer the question you want to be asked**. Reframe it into one that you're comfortable answering. [Don't Think of an Elephant!](https://www.goodreads.com/book/show/13455.Don_t_Think_of_an_Elephant_Know_Your_Values_and_Frame_the_Debate) is an excellent book on framing issues.
2. **Stay positive**, find a positiver framing and stick to it.
3. **Speak in threes**. Narrow your message in three concise points.

#### Model, document and share

**Model**. Start measuring your team's health (maybe using short, monthly surveys) and your team's throughput (do some lightweight form of task sizing), baseline before your change.

Then just start running Kanban. Don't publicise it, don't make a big deal about it, just start doing it. Frame it as a short experiment.

**Document**. Document the problem you set out to solve, the learning process, and the details of how another team would adopt the practice.

**Share**. The final step is to share your documented approach, don't lobby for change, just present the approach and your experience following it. This has often lead to more adoption than top-down mandates have.


##### Where it works

Compare it with the top-down mandate. Mandates assume:
* **It's better to adopt a good-enough approach quickly**
  * Teams have the bandwidth to adopt a new approach
  * The organisation has available resources to coordinate a rollout
  * You want to centralise decision-making
  * Consistency is important
  * It's important to make this change quickly
* **Model, document, share assumes**
  * Some teams don't have the bandwidth to adopt a new approach
  * The organisation may not have resources to coordinate a rollout
  * You want to decentralise decision-making
  * Teams have agency to adopt practices for themselves
  * It's okay to approach change gradually

  You'll still need some natural authority and the respect of your peers.

  Do not try to use this as a strategy to circumvent organisational authority, it does not end well.

  #### Scaling consistency: designing centralised decision-making groups

  As organisations grow, there is a subtle slide into inconsistency