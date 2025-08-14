# matsengrp subagents for Claude Code

[Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) are a useful feature of Claude Code that save you tokens in your primary context window while providing instructions for a specialized task.

[This video](https://www.youtube.com/watch?v=Pif98jOScYc) provides a nice introduction.


## Example Uses

```
> @agent-topic-sentence-stickler please check @main.tex
```

```
> @agent-clean-code-reviewer please review the current PR, limiting scope to just the changed files
```

```
> @agent-pdf-question-answerer please read Koenig2017.pdf and tell me how they determined antibody binding affinity
```


## Available Agents

• **clean-code-reviewer** - Expert code review focusing on Uncle Bob's clean code principles, DRY violations, and maintainability
• **scientific-tex-editor** - Expert scientific editing for LaTeX documents following Matsen group writing guidelines  
• **tex-grammar-checker** - Meticulous line-by-line grammar checking for LaTeX academic documents
• **tex-verb-tense-checker** - Reviews LaTeX documents for verb tense consistency in scientific writing
• **topic-sentence-stickler** - Ensures strong topic sentences and paragraph structure in academic papers
• **pdf-question-answerer** - Analyzes scientific PDFs to extract information and answer research questions
• **journal-submission-checker** - Pre-submission quality checks for repositories, references, and bibliographic info
• **pdf-proof-reader** - Meticulous proofreading of PDF galley proofs for grammatical errors and typos only


## Installation

To "install", link to the `agents` subdir of your home `.claude` directory, assuming you don't have agents already:

    git clone git@github.com:matsengrp/claude-code-agents.git
    cd claude-code-agents
    ln -s $PWD ~/.claude/agents


The subagents that read PDFs require [pdf-navigator-mcp](https://github.com/matsengrp/pdf-navigator-mcp).


## Contributing

If you have agents you'd like to share, or improvements to these agents, we'd love to get PRs!
