# PowerPoint Automation

UiPath Studio Windows workflow based on Studio-generated PowerPoint and Excel activities. It reads Excel data, opens a presentation template, adds dynamic slides/text and a data table/chart payload, saves the presentation, and exports PDF.

Input: `Template/Gradebook.xlsx` and `Template/PresentationTemplate.pptx`.
Output: `Output/GeneratedPresentation.pptx` and `Output/GeneratedPresentation.pdf`.

Validation: the template is now a genuine native `.pptx` file. Package publication still reports invalid activity configuration, so no Robot runtime claim or output verification is made.
