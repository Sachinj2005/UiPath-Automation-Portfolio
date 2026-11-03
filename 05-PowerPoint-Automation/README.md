# PowerPoint Automation

UiPath Studio Windows workflow based on Studio-generated PowerPoint and Excel activities. It reads Excel data, opens a presentation template, adds dynamic slides/text and a data table/chart payload, saves the presentation, and exports PDF.

Input: `Template/Gradebook.xlsx` and `Template/PresentationTemplate.pptx`.
Output: `Output/GeneratedPresentation.pptx` and `Output/GeneratedPresentation.pdf`.

Validation: the template is a valid native `.pptx` package. The missing `InsertSlide.LayoutName` was corrected; package `1.0.4` publishes successfully. Robot reaches the PowerPoint scope but fails with `TYPE_E_CANTLOADLIBRARY` while loading the PowerPoint COM type library. No presentation/PDF output was verified; Office repair is required before retesting.
