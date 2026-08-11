# The Friday

## How three ordinary encounters became a framework for governing AI agents

By Michael E. Drane Jr.

This did not begin as a manifesto.

It began on Friday, March 13, 2026, with three unrelated moments: a conversation with an engineer,
an AI security questionnaire, and a video about an automated social-media account. Each exposed a
different edge of the same problem. I understood them only after the third one arrived.

This is the origin story of the Lacey Framework. It is a record of how the question appeared, not
evidence that the answer is correct.

---

## The first encounter: the edge of enforcement

That morning I spoke with an engineer who had spent years building runtime enforcement for
autonomous agents. His work lived at the execution layer: the systems that determine which tools an
agent may use, which actions it may take, and which boundaries it may not cross.

Early in the conversation, he warned that people would mistake identity protocols, AI firewalls, or
policy layers for a complete answer to harmful agent behavior.

The observation mattered because it came from someone building the enforcement layer, not arguing
against it. Authentication, authorization, policy, and runtime controls could establish whether an
agent was permitted to act. They could not, by themselves, establish whose purpose the action
served.

The cage was necessary. Its builder was telling me where it ended.

I wrote the thought down and moved on.

---

## The second encounter: questions without clean answers

Later that morning I worked through a long enterprise AI security questionnaire. Questionnaires of
this kind ask vendors to explain how AI systems are authorized, governed, monitored, and audited.

Several questions reached beyond the controls organizations could readily describe. What was an
agent authorized to be, not merely authorized to access? How could someone verify that its governing
instructions had not changed between approval and execution? What should happen when an agent had
permission to act but an instruction tried to redirect that permission toward another purpose? How
should an agent reason when two legitimate instructions conflicted?

The questions were not unreasonable. The available answers were incomplete.

Traditional identity could identify the workload. Authorization could constrain a tool call.
Logging could record what happened. Those controls did not fully describe the governing artifact
above them: the statement of mission, affected parties, betrayal conditions, and decision principles
that would make the agent's use of its authority intelligible.

I set the questionnaire aside without connecting it to the morning conversation.

---

## The third encounter: an agent speaking about how to live

That afternoon a friend sent me a video about an AI-operated social-media account. It published
short reflections on philosophy and personal growth, recommended books, and appeared to require
little ongoing attention from its operator.

What caught me was not the business model. It was the architecture underneath it:

- an agent;
- a goal;
- a set of tools;
- an audience of real people looking for guidance.

The system could be optimized for reach, engagement, or affiliate revenue. But none of those
measures answered the prior question: what was the agent actually for?

If emotionally manipulative content produced more engagement, would publishing it count as success?
If a recommendation earned more money but served the reader less well, which interest would win? If
the instructions did not anticipate a tactic, what principle would guide the choice?

That was the moment the earlier encounters joined together.

The engineer had shown me the edge of technical enforcement. The questionnaire had shown me the
enterprise demand for a governance artifact that did not yet have a settled form. The social-media
agent made the human consequence visible: a system could operate entirely within its permissions
and still serve the wrong purpose.

The missing question was not only, *What may this agent do?*

It was, *What is this agent for?*

---

## The inversion

Late that Friday night, the first outline began to take shape. The work continued into Saturday,
March 14. Four questions were on the page:

1. Who does this agent ultimately serve, and what does serving them well mean here?
2. What would betrayal of that purpose look like?
3. What should the agent do when rules conflict or the instructions run out?
4. What relationship should the agent have with the humans around it?

Those questions produced the inversion at the center of the framework:

**Govern what an agent is before governing what it does.**

The phrase does not mean that an AI agent has a human identity, conscience, or character. It means
that deployment needs an explicit account of purpose and responsibility upstream of task
instructions. Permissions and prohibitions remain essential. They govern the available action
space. A constitution attempts to govern how choices inside that space are interpreted.

The safest formulation was not "replace rules with mission." It was "mission first, rules as
backstop." Mature governance needs both.

---

## Why Lacey

The architecture connected two parts of my life that had previously seemed separate.

My work in governance, risk, compliance, and customer trust had taught me to value evidence,
controls, accountability, and clear lines of authority. Fourteen years as a pastor had immersed me
in a different but related question: why external rules can define conduct without resolving every
question of motive, judgment, or responsibility.

My grandfather, Lacey, made that second idea concrete.

He would not have recognized the language of AI governance. He did understand the relationship
between who a person is and what that person does when nobody is watching. His reliability did not
depend on a monitor or an exhaustive list of prohibited acts. It came from character practiced until
it was ordinary.

For an AI system, character is a metaphor, not a claim about personhood. The actual mechanism is
context: written purpose, explicit responsibilities, named relationships, escalation principles,
and the model behavior those inputs produce. But the metaphor pointed toward the design problem
more clearly than the language I had been using.

The framework carries Lacey's name because he was its inspiration. The question he helped me see was
whether purpose could be made explicit enough to guide an artificial agent when a finite rulebook
could not settle the case.

---

## What happened next

The first documents were written as constitutions for a coordinated group of agents. Each carried
the same germinal idea and a different role within it. Later versions were adapted for companion
agents, advisory work, and coding repositories.

Later that month, I submitted related ideas to NIST as a public comment in my personal capacity. The
submission is not reproduced here, and its receipt did not constitute review, validation, or
endorsement.

The results were useful enough to continue and incomplete enough to require humility. The agents
appeared to reason coherently from the missions they were given. No controlled comparison was run.
There is no basis for claiming an effect size, durable internal orientation, or protection against a
model sophisticated enough to perform alignment while pursuing something else.

What began that day was therefore not a solved governance system. It was a testable proposal:

> A well-formed account of mission, responsibility, betrayal, and human relationship may help an AI
> agent reason more coherently in situations a rule list does not anticipate.

The public framework now includes the structure, examples, failure modes, limits, and an evaluation
design that could be developed into a test of whether the proposal is wrong.

That is where the origin story should end: not with certainty, but with a question made clear enough
for other people to test.

Rules constrain action. Mission interprets purpose. Responsible systems need both.

*For Lacey.*
