# v0 - Vercel's AI-Powered UI Generation Assistant

This directory contains documentation about v0, Vercel's AI system for generating and editing Next.js applications.

## Documentation Overview

### 📖 [HOW-V0-WORKS.md](./HOW-V0-WORKS.md) - **START HERE**
**Complete technical architecture and workflow explanation**

This document answers the key question: **"What happens technically when a user adds a prompt, and how is code being generated and edited?"**

Topics covered:
- Complete workflow from user prompt to generated code
- The 7 architectural layers explained
- What's in the "middle layer" between prompt and app code
- How the AI model (GPT-4o) processes requests
- How code is generated using MDX components
- Vercel's rendering engine (the secret sauce)
- How editing and iteration works
- Specialized sub-agents (TodoManager, SearchRepo, etc.)
- Technical constraints and capabilities
- Data flow diagrams and concrete examples

**Perfect for:** Understanding v0's technical architecture, learning how AI-powered code generation works, and grasping the full system design.

---

### 📝 System Prompts

#### [2025-08-11-prompt.md](./2025-08-11-prompt.md)
**Latest v0 system prompt** (August 2025)

Contains the most recent system prompt with:
- Tool use formatting (MDX components)
- Available sub-agents (TodoManager, SearchRepo, ReadFile, InspectSite, SearchWeb, FetchFromWeb)
- Detailed tool descriptions and schemas
- Usage patterns and examples

#### [2025-04-05/](./2025-04-05/)
**Earlier v0 documentation** (April 2025)

Contains:
- `v0.md` - Core system prompt and instructions
- `v0-model.md` - AI model integration details (GPT-4o, AI SDK)
- `v0-tools.md` - MDX component tools (CodeProject, QuickEdit, etc.)
- `instructions.md` - Additional detailed instructions

---

## Quick Reference

### What is v0?
v0 is Vercel's AI-powered assistant that generates complete Next.js applications from natural language prompts and screenshots. It can create, edit, and iterate on full-stack web applications entirely in your browser.

### Key Technologies
- **AI Model:** GPT-4o (OpenAI)
- **Framework:** Next.js App Router + React
- **Styling:** Tailwind CSS + shadcn/ui
- **Icons:** Lucide React
- **AI Integration:** Vercel AI SDK
- **Runtime:** Browser-based Next.js (WebContainers)

### Key Capabilities
- Generate UI components from text descriptions
- Recreate designs from screenshots
- Create full-stack Next.js applications
- Make iterative edits through natural language
- Support for Server Components, API Routes, Server Actions
- Responsive and accessible by default
- Real-time preview and hot reload

### Architecture Highlights

```
User Prompt → GPT-4o → MDX Components → Vercel Renderer → Browser Runtime → Live App
```

The "secret sauce" is Vercel's custom rendering engine that:
1. Parses MDX component output from the AI
2. Manages a virtual file system in the browser
3. Runs a lightweight Next.js runtime
4. Compiles and renders code in real-time
5. Enables instant iteration and editing

---

## Learning Path

1. **Want to understand how v0 works?**  
   → Read [HOW-V0-WORKS.md](./HOW-V0-WORKS.md)

2. **Want to see the latest system prompt?**  
   → Check [2025-08-11-prompt.md](./2025-08-11-prompt.md)

3. **Want to understand the AI model integration?**  
   → See [2025-04-05/v0-model.md](./2025-04-05/v0-model.md)

4. **Want to know about MDX components?**  
   → Read [2025-04-05/v0-tools.md](./2025-04-05/v0-tools.md)

5. **Want detailed instructions and rules?**  
   → Check [2025-04-05/v0.md](./2025-04-05/v0.md)

---

## Related Resources

- [Vercel AI SDK Documentation](https://sdk.vercel.ai)
- [v0.dev Official Site](https://v0.dev)
- [Next.js Documentation](https://nextjs.org/docs)
- [shadcn/ui Components](https://ui.shadcn.com)

---

## Contributing

This documentation is part of the [awesome-ai-system-prompts](https://github.com/guyb1/awesome-ai-system-prompts) repository. Contributions, corrections, and updates are welcome!

---

*Last updated: January 2026*
