# placed-resume-builder

Build and manage professional resumes with AI assistance.

## Tools

- `create_resume` - Create new resume from profile or scratch
- `get_resume` - Retrieve resume by ID
- `update_resume` - Update any resume section
- `list_resumes` - List all your resumes
- `get_resume_schema` - Understand available sections
- `list_resume_templates` - Browse 37 templates
- `get_template_preview` - Preview template details
- `change_resume_template` - Switch resume template
- `get_resume_pdf_url` - Download as PDF
- `get_resume_docx_url` - Download as Word
- `export_resume_json` - Export as JSON
- `export_resume_markdown` - Export as Markdown

## Quick Start

1. **Create a resume:**
   ```
   create_resume(title="Senior Engineer Resume", target_role="Staff Engineer")
   ```

2. **Update sections:**
   ```
   update_resume(resume_id="...", experience=[...], skills=[...])
   ```

3. **Choose template:**
   ```
   list_resume_templates()
   change_resume_template(resume_id="...", template_id="modern")
   ```

4. **Export:**
   ```
   get_resume_pdf_url(resume_id="...")
   export_resume_markdown(resume_id="...")
   ```

## Resume Sections

All sections are optional and can be updated independently:
- basics (name, email, phone, headline, location)
- summary (professional overview)
- experience (work history)
- education (degrees and certifications)
- skills (technical and soft skills)
- languages (language proficiencies)
- certifications (professional certs)
- awards (honors and recognition)
- projects (personal/professional projects)
- publications (articles, papers, books)
- references (professional references)
- volunteer (volunteer experience)
- interests (hobbies and interests)
- profiles (LinkedIn, GitHub, etc.)

## Tips

- Use `get_resume_schema()` to see all available fields
- Quantify achievements with metrics (numbers, percentages, dollars)
- Use action verbs at the start of bullet points
- Mirror job description language for better matching
- Test ATS compatibility with `check_ats_compatibility()`
