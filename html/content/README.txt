Put site images in this folder with these names (JPG):

hero.jpg                    wide banner photo behind the top of every page (about 2400 x 1200)
portrait.jpg                your photo next to the bio (square, about 900 x 900; included)

Project tiles (cropped to 4:3, about 1200 x 900 is plenty):
internal-displacement.jpg   Mapping Climate-Driven Internal Displacement
two-child-policies.jpg      Two-Child Policies in India
compounding-shocks.jpg      Compounding Climate Shocks in Bangladesh
forests.jpg                 Forests and Sustainable Development
groundwater.jpg             Ground Water Dynamics
women-in-water.jpg          WBG Women in Water
climate-hazards.jpg         Climate Hazards
urbanization.jpg            Urbanization
fragile-conflict.jpg        Fragile and Conflict-Affected Areas

Art tab, photographs from Kurli, in content/kurli/:
kurli-01.jpg ... kurli-04.jpg     included; shown at their own shape, full image when clicked
                                  to add more, copy a <figure class="shot"> block in index.html

Art tab, paintings, in content/art/:
art-01.jpg ... art-06.jpg         included; shown at their own shape. Larger scans (1200px+) will look sharper.

Captions are in index.html: search for "Caption:" and "Title, medium, year".

Resume tab:
Kurli_Resume.pdf                  the file visitors download
resume/Kurli_Resume-1.png, -2.png page images shown on the Resume tab
After replacing the PDF, regenerate the page images (from the html/content folder):
    pdftoppm -png -r 160 Kurli_Resume.pdf resume/Kurli_Resume
(pdftoppm is in poppler-utils / `brew install poppler`.) If the page count changes,
add or remove <img> lines in the Resume section of index.html.

To use other names or .png files, change the src="content/..." paths in index.html.
