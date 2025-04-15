# Hedera Vibe-Code with Cline

Starter repo for vibe coding a Hedera application using Cline.

Have you built something using this repo as a starting point?
Let us know, we'd love to hear about it.
Create an issue on this repo, or a PR to add link to your project in the README for this project!

## How to use this repo

This repo comes with a bare-bones starting point for AI Agentic Development using Cline.

Cline is a visual studio code plugin that is designed to assist you in developing applications using generative AI.

### Using the Github repo

Press the "Fork" button in Github.

Enter the following commands - replace `${YOUR_GITHUB_USERNAME}` with your Github username.

```shell
git clone --single-branch -b main https://github.com/${YOUR_GITHUB_USERNAME}/hedera-vibe-code-cline
cd ./hedera-vibe-code-cline
code ./
```

(For example, as my Github username is `bguiz`, the first command for me would be: `git clone --single-branch -b main https://github.com/bguiz/hedera-vibe-code-cline`)

Next, override this `README` file with your own.
A sample starter file has been provided for you:

```shell
mv ./README.md ./README.original.md
mv ./README.template.md ./README.md
```

Edit the `README.md` file, following the instructions in the template.

### Using Cline within VS code

Click on the Cline icon in the left column, and begin prompting.
This repo is ready to go!

If you're a bit more meticulous, before you start prompting:

- Look at `.clinerules.md`
  - This is a file that Cline will use as its "system prompt" to the LLM, and guides how you want it to behave.
- Look at `docs/prd.md`
  - This is the product requirements document (PRD)
  - Want to find out more about what makes for a great PRD? Recommended article: [How to create a product requirements document (PRD) - Dan Radigan](https://www.atlassian.com/agile/product-management/requirements)
- Look at `docs/architecture.md`
  - This is the technical architecture document
  - Want to find out more about what makes for a great technical architecture document? Recommended article: [arc42 Template Overview](https://arc42.org/overview)
- Look at `docs/tasks.md`

Note that all of these files are initially a default template.
If the set values do not work for you, feel free to modify them *before* you start prompting Cline.
Alternatively, you can ask Cline itself to help you to flesh out these documents, via prompts, prior to prompting it to start development tasks.

## How to set up Cline for the first time

If you have not used Cline before, you will need to set it up.

## Prerequisites to installing Cline

- [ ] [VS code](https://code.visualstudio.com/)
- [ ] [OpenRouter](https://openrouter.ai/) account
  - Note that you can use individual LLM provider's API keys, *or* a local instance of an LLM too
  - However, these steps assume that you're using OpenRouter

### Steps to install Cline

(1) Install cline: https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev

- This is a VS code extension

(2) In VS code press the cline bot icon, and it opens up a vertical column

(3) In the intro setup/ config, "use API key", then select "openrouter", then get an openrouter API and paste that in

- Log in to [OpenRouter](https://openrouter.ai/)
- Navigate to [`openrouter.ai/settings/keys`](https://openrouter.ai/settings/keys)
- Press the "Create Key" button
- Copy this API key and store it somewhere safe

(4) You should now see "what can I do for you?" at the top, and "Auto approve: None" at the bottom, followed by a chat box. Underneath the chat box there are some symbols.

- `@` to insert special commands into the chat box
- camera icon to insert an image
- 3 stacked rectangles to select MCP servers
- the name of the selected model, which should be `openrouter:...` at the moment
- a toggle button to switch between "plan" and "act" modes

(5) Click on the model name at the bottom

- In the "model" drop down, select "anthropic/claude-3.7-sonnet:thinking"
- Select "enable extended thinking"
- Drag the "budget" slider all the way to the right to max out the allowed tokens (6524 tokens)
- Click on the model name at the bottom again to save and close these selections

(6) Select "auto-approve"

- By default it starts as "none"
- There is a checklist of items which you can select: read, edit, commands, browser, and MCP
- Select whichever *subset* of these you're most comfortable with, or leave it as none
- When cline wants to perform these actions, and it doesn't have these permissions, it will ask you each time
- For "max requests", the default is "20". type "100" to allow it to make a larger number of prompts before asking you for permission to continue.

(7) Select "plan" mode from the plan-act toggle button if you wish to begin planning, but without implementation.

(8) Select "act" mode from the plan-act toggle button if you wish to switch to implementation.

(9) Now you're ready to work with Cline!

## Author

[Brendan Graetz](https://blog.bguiz.com/)

## Licence

MIT
