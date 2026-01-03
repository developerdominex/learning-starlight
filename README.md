# Starlight MD Converter

**Description:**
Starlight MD Converter is a tool that allows developers to write documentation in a simple DSL called SLMD 
and convert it into ready-to-use Markdown files. This is especially useful for maintaining structured 
documentation or tutorials without manually writing Markdown syntax.

## Pros of Starlight MD Converter


- Simplifies writing documentation using intuitive tags.
- Automatically converts SLMD to proper Markdown syntax.
- Supports headings, bold, italic, code blocks, links, lists, colors, and tables.
- Allows developers to focus on content instead of Markdown formatting.
- Quick conversion for large documents or tutorials.


## Usage Steps

**Step 1: Write your SLMD file**
Create a new file with the extension `.slmd`. Use the following tags:


- &lt;big1&gt;, &lt;big2&gt;, &lt;big3&gt; for headings of different levels.
- &lt;bold&gt;Bold text&lt;/bold&gt; to highlight important points.
- &lt;italic&gt;Italic text&lt;/italic&gt; for emphasis.
- &lt;code&gt;Inline code&lt;/code&gt; for commands or snippets.
- &lt;color colorname&gt;Colored text&lt;/color&gt; to indicate colored highlights (optional, shows fallback).
- &lt;link https://example.com&gt;Example Link&lt;/link&gt; to insert clickable links.
- &lt;ul&gt;&lt;li&gt;Item&lt;/li&gt;&lt;/ul&gt; to create lists.
- &lt;table&gt;&lt;tr&gt;&lt;td&gt;Cell&lt;/td&gt;&lt;/tr&gt;&lt;/table&gt; to create tables.


**Step 2: Save the SLMD file**
Save the file with a descriptive name, e.g., `documentation.slmd`.

**Step 3: Create a conversion script (program.sl)**
Use Starlight CLI to create a script that reads the SLMD file and outputs Markdown:

`
import { convertFile } from "starlight-mdconverter"

sldeploy "=== SLMD to Markdown Converter ==="

let inputFile = ask("Enter path to your .slmd file:")
let outputFile = ask("Enter path for output .md file:")

convertFile(inputFile, outputFile)

sldeploy "Conversion complete! Markdown file saved."
`

**Step 4: Run the converter**
Open the terminal and execute your `program.sl` with Starlight CLI:

`starlight program.sl`

Follow the prompts:

- Provide the full path to your SLMD file.
- Provide the full path and filename for the output Markdown file.


**Step 5: Verify the output**
After conversion, open the generated `.md` file in any Markdown editor or viewer. 
All your SLMD formatting should now be properly converted into Markdown syntax.

## Example Table in SLMD

Feature | Supported
--- | ---
Headings | Yes
Bold & Italic | Yes
Code | Yes
Links | Yes
Lists | Yes
Tables | Yes
Colors | Yes (fallback in Markdown)

## Tips for Developers


- Write content in SLMD naturally; the converter handles Markdown syntax automatically.
- Use colors only for readability in SLMD; Markdown will show the color name as fallback.
- Keep consistent file naming for easier management.
- Test conversion frequently with small SLMD files before working on large documents.


## Conclusion

Starlight MD Converter streamlines writing documentation, tutorials, or notes. 
It allows developers to focus on content rather than Markdown formatting, while ensuring a clean, ready-to-use Markdown output.
