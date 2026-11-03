# PowerPoint Automation

UiPath Studio Windows workflow based on Studio-generated PowerPoint and Excel activities. It reads Excel data, opens a presentation template, adds dynamic slides/text and a data table/chart payload, saves the presentation, and exports PDF.

Input: `Template/Gradebook.xlsx` and `Template/PresentationTemplate.pptx`.
Output: `Output/GeneratedPresentation.pptx` and `Output/GeneratedPresentation.pdf`.

Validation: `Main.xaml` passed XML parsing and UiPath command-line structural analysis. Runtime is pending because the checked-in presentation is a safe placeholder fixture rather than a native PowerPoint document; replace it with a real `.pptx` template in Studio before attended execution.
