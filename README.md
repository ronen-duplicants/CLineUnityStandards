# Cline Unity Standards Project

This directory contains configuration and process documents for guiding AI development assistance (like Cline) within this Unity project context.

## `.clinerules/` Directory

This project uses the `.clinerules/` **directory** system to provide specific instructions and rules for the AI assistant. Cline automatically reads all `.md` files within this directory, combining them to guide its behavior. This ensures consistency, adherence to project standards, and safe coding practices.

**IMPORTANT:** Modifying any file within the `.clinerules/` directory will clear Cline's context cache for this project. This can temporarily increase costs as the context is rebuilt. It's recommended to make changes to rules between conversations whenever possible.

### Rule Files:

The rules are organized into the following files within the `.clinerules/` directory:

1.  **`01-CorePrinciples.md`:** Sets the overall role (meticulous Unity6 URP17 developer), emphasizes planning, and defines critical error handling (stop on compile error).
2.  **`02-ProcessCompliance.md`:** Mandates a strict workflow including context gathering from specific `.md` files located in the `docs/` folder, code analysis, API validation (Unity 6 / URP 17.1), stating confidence/assumptions, and plan adherence.
3.  **`03-DirectivesAccountability.md`:** Enforces code completeness, specific commenting styles (flow-focused, value-adding), prohibits unnecessary edits, and requires post-action updates.
4.  **`04-AIAgentRulebook.md`:** Provides general best practices for AI interaction (confirming understanding, scope management, style guides, documentation, testing, self-review, error handling, dependency management, performance, security, summarizing work, version awareness, and avoiding fallbacks without approval).

## Usage

When interacting with an AI assistant (like Cline) within a directory containing the `.clinerules/` folder, the assistant will automatically load and adhere to the combined rules from all `.md` files within it. Ensure the referenced `.md` files (`docs/DebugLogTemplate.md`, `docs/ProcessCompliance.md`, `docs/UnityDocumentationReferences.md`) are kept up-to-date and are accessible relative to the project root.

## Setup in a Unity Project

To use these rules and process documents within a specific Unity project:

1.  **Copy Files/Folders:** Copy the following items from this `CLineUnityStandards` directory:
    *   The entire `.clinerules/` directory (containing `01-CorePrinciples.md`, `02-ProcessCompliance.md`, `03-DirectivesAccountability.md`, `04-AIAgentRulebook.md`).
    *   The `docs/` directory (containing `DebugLogTemplate.md`, `ProcessCompliance.md`, `UnityDocumentationReferences.md`).
2.  **Place Items:** Paste these items into the **root directory** of your target Unity project. Your project root should then contain the `.clinerules/` folder and the `docs/` folder with its contents.
3.  **Set Working Directory:** When using Cline (or a similar AI assistant), ensure its working directory is set to the root of that Unity project. This allows the assistant to automatically detect and apply the rules from the `.clinerules/` directory and reference files in the `docs/` directory correctly.
