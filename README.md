# vibewriting
## Cursor Writing Workspace: A Framework for Strategic AI-Powered Content

This repository provides a template and methodology for using the Cursor code editor as a powerful, framework-driven writing assistant. It's designed for professionals in sales, marketing, and content creation who want to leverage AI to produce high-quality, consistent, and strategically-aligned written materials.

The core idea is to move beyond generic prompts and build a "second brain" where the AI acts as a strategic partner, following your specific rules, methodologies, and reference materials.

## Why This Approach?

- Standard interactions with AI tools often result in generic, inconsistent, or "salesy" content. This workspace solves that by:
- Enforcing Consistency: By grounding the AI in your specific frameworks (like Gap Selling, as shown in the video), you ensure every piece of content follows your proven methodologies.
- Maintaining Context: The working-memory system allows the AI to manage multiple conversations or projects simultaneously without losing track of context, progress, or objectives.
- Scaling Quality Outreach: Generate personalized, value-driven emails, blog posts, and discovery questions at scale, without sacrificing quality.
- Reducing Hallucinations: Providing specific reference documents dramatically reduces the chances of the AI making things up, as its knowledge is anchored to your provided materials.

Automating Process: The AI not only writes the content but also helps structure the entire engagement, from initial planning to follow-up sequences.

## Key Components

The power of this system comes from its structured organization:

1. .cursor/rules/

This is the command center for instructing the AI agent.

- systemprompt.mdc: This is the meta-prompt that governs the AI's overall behavior. It tells the AI how to think and act—to break down tasks, create a plan, ask clarifying questions, and utilize the workspace structure. It's set to "Always Apply".

- emailprompt.mdc (Example): This is a task-specific prompt. It contains detailed instructions for a particular type of task, like writing a sales email. It defines the reference documents, core instructions, process steps, quality gates, and desired output format. You can create different rule files for different tasks (e.g., blogpost.mdc, linkedin_post.mdc).

2. docs/

This directory serves as the AI's knowledge base.

- frameworks/: Contains the core methodologies and principles you want the AI to follow. In the video, this holds gap_selling.md.

- references/: Stores supporting documents, articles, case studies, or any other information that can provide context for a task.

- templates/: Holds boilerplate or structural examples for different types of content.

- working-memory/: This is where the magic happens. The AI creates a subdirectory for each new, complex task (e.g., jim-yarrow-engagement). Inside, it maintains:
working-memory/plan: A living document where the AI tracks the project's status, objectives, context, and a to-do list.
working-memory/Generated Files: The AI places its output files here, such as draft emails, conversation frameworks, and discovery questions.

##Setup and Usage

Follow these steps to get your own AI writing workspace up and running.

### Prerequisites

You must have the Cursor editor installed.

### Step-by-Step Guide

1. Clone the Repository:

Generated bash
```git clone https://github.com/rpiplewar/vibewriting.git```


2. Open in Cursor:
- Launch Cursor.
- Click "Open Project" and select the cursor-writing-workspace folder you just cloned.

3. Customize Your Frameworks:
- Navigate to the docs/frameworks/ directory.
- Edit or replace the example gap_selling.md with your own sales playbooks, writing style guides, brand voice guidelines, or any other core methodology.

4. Populate Your Knowledge Base:
- Add relevant documents to docs/references/.
- Add content structure examples to docs/templates/.

5. Initiate a Task:
- Open the Chat panel in Cursor (Cmd+K or Ctrl+K).
- Write a clear, concise prompt describing your goal. Crucially, reference your framework files using the @ symbol.

Example Prompt :

I met John Snow at a conference. He's interested in AI traffic segregation in Google Analytics. I want to engage him in a conversation based on @docs/frameworks/gap_selling.md. He has already set up a technical guide which I have at @docs/references/technicalguide.md. We want to engage him in a conversation.

6. Collaborate with the AI:
- The AI will first create a plan and a dedicated working-memory folder for the task.
- It will then generate the required documents (e.g., an outreach email framework, discovery questions, and the final email draft).
- Review the generated files. You can provide feedback directly in the chat, and the AI will iterate on its work based on your instructions and the rules you've set.

Example Walkthrough: The "John Snow" Case

The above prompt resulted in the AI performing the following actions automatically:
1. Created a plan to analyze the request and apply the Gap Selling framework.
2. Created a new directory: docs/working-memory/john-snow-engagement/.
3. Generated a plan.md file inside it to track the conversation's state.
4. Generated gap-selling-conversation-framework.md to outline the entire sales engagement strategy.
5. Generated first-outreach-message.md, which included multiple subject line options and a full email body aligned with the "give value, don't ask for time" principle.
6. Generated discovery-questions-toolkit.md to prepare the user for the subsequent conversation.

This structured, multi-file output is far more powerful than a single, simple text response, turning a writing task into a fully-planned strategic engagement.