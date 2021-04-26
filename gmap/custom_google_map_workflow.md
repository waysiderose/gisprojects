# Custom Basemap Using Google

Customizing a basemap can be done in multiple ways. Previously, I used ArcGIS Esri software to do this. However, what if the client does not have a license?

Purpose: Customize a basemap to the stylistic colors of an organization. 

## Step 1: Chose an organization.

I chose the non-profit <a href ="https://www.globallinks.org/">Global Links</a>. They do good work that has local and far reaching impact - for example, they are a primary mask supplier for an organization I volunteer with.

## Step 2: Create a color pallet.

To get a reference image, I took a screen shot of the main page of Global Links.

<img src="/gmap/GlobalLinksImpage.PNG" width="900"/>

Created a color pallet reference table with a Column for the Hex Code, Color Name, Sample Image, and RBG Distribution. The below reference table was used as a code pallet for which hex codes to use to assign colors in the map style editor.

#### Abbreviated Color Pallet Example

 <table style="border-collapse:collapse;border:none;">
    <tbody>
        <tr>
            <td style="width: 85.25pt;border: 1pt solid windowtext;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;text-align:center;'><strong><span style="font-size:19px;">Hex Code</span></strong></p>
            </td>
            <td style="width: 125.85pt;border-color: windowtext windowtext windowtext currentcolor;border-style: solid solid solid none;border-width: 1pt 1pt 1pt medium;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;text-align:center;'><strong><span style="font-size:19px;">Color Name</span></strong></p>
            </td>
            <td style="width: 149.9pt;border-color: windowtext windowtext windowtext currentcolor;border-style: solid solid solid none;border-width: 1pt 1pt 1pt medium;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;text-align:center;'><strong><span style="font-size:19px;">Color</span></strong></p>
            </td>
            <td style="width: 106.5pt;border-color: windowtext windowtext windowtext currentcolor;border-style: solid solid solid none;border-width: 1pt 1pt 1pt medium;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;text-align:center;'><strong><span style="font-size:19px;">RBG Color Code</span></strong></p>
            </td>
        </tr>
        <tr>
            <td rowspan="3" style="width: 85.25pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;height: 21pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">#8C264B</span></p>
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">&nbsp;</span></p>
            </td>
            <td rowspan="3" style="width: 125.85pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 21pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Stiletto</span></p>
            </td>
            <td rowspan="3" style="width: 149.9pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 21pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIUAAABTCAIAAAA+31NZAAAAAXNSR0IArs4c6QAAAUdJREFUeF7t3cEJgEAQxVDXjmzG1qx07+JFsQIDvqkgJPzzjDnn4jIG1gwJkMvAuPdxbDslnxuwj88TvAD00KNloEVjH3q0DLRo7EOPloEWjX3o0TLQorEPPVoGWjT2oUfLQIvGPvRoGWjR2IceLQMtGvvQo2WgRWMferQMtGjsQ4+WgRaNfejRMtCisQ89WgZaNPahR8tAi8Y+9GgZaNHYhx4tAy0a+9CjZaBFYx96tAy0aOxDj5aBFo196NEy0KKxDz1aBlo09qFHy0CLxj70aBlo0diHHi0DLRr70KNloEVjH3q0DLRo7EOPloEWjX3o0TLQorEPPVoGWjT2oUfLQIvGPvRoGWjR2IceLQMtGvvQo2WgRWMferQMtGjsQ4+WgRaNfejRMtCisY9Wj+dfaovrrzT20Sqvhx4tAy0a+9CjZaBFcwInOwpfvewtMgAAAABJRU5ErkJggg==" alt="image" width="133"></span></p>
            </td>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 21pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">R: 140</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 21pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">B: 38</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 21pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">G: 75</span></p>
            </td>
        </tr>
        <tr>
            <td rowspan="3" style="width: 85.25pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;height: 16.5pt;vertical-align: top;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style='font-size:16px;font-family:"Calibri",sans-serif;'>#04B2D9</span></pre>
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">&nbsp;</span></p>
            </td>
            <td rowspan="3" style="width: 125.85pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 16.5pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Cerulean</span></p>
            </td>
            <td rowspan="3" style="width: 149.9pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 16.5pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIEAAABCCAIAAAD/viIdAAAAAXNSR0IArs4c6QAAAPZJREFUeF7t00ENACAQxEAg+BeDG9wQVPQzGLimZec+d3ipgZVed/wb0KD/Bxpo0BvoCexAg95AT2AHGvQGegI70KA30BPYgQa9gZ7ADjToDfQEdqBBb6AnsAMNegM9gR1o0BvoCexAg95AT2AHGvQGegI70KA30BPYgQa9gZ7ADjToDfQEdqBBb6AnsAMNegM9gR1o0BvoCexAg95AT2AHGvQGegI70KA30BPYgQa9gZ7ADjToDfQEdqBBb6AnsAMNegM9gR1o0BvoCexAg95AT2AHGvQGegI70KA30BPYgQa9gZ7ADjToDfQEdqBBb6AnsIO+wQMdRwITKxxYsQAAAABJRU5ErkJggg==" alt="image" width="129"></span></p>
            </td>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 16.5pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">R: 4</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 16.5pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">B: 178</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 16.5pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">G: 217</span></p>
            </td>
        </tr>
        <tr>
            <td rowspan="3" style="width: 85.25pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;height: 0.25in;vertical-align: top;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style='font-size:16px;font-family:"Calibri",sans-serif;'>#03738C</span></pre>
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">&nbsp;</span></p>
            </td>
            <td rowspan="3" style="width: 125.85pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 0.25in;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Blue Lagoon</span></p>
            </td>
            <td rowspan="3" style="width: 149.9pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 0.25in;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAIAAAABICAIAAACx52pFAAAAAXNSR0IArs4c6QAAAQNJREFUeF7t01kNACAQxUAOydhANEFFf2YNNGn3zX3ucJ2B1aGRvwEB4j8QQIDYQIy3AAFiAzHeAgSIDcR4CxAgNhDjLUCA2ECMtwABYgMx3gIEiA3EeAsQIDYQ4y1AgNhAjLcAAWIDMd4CBIgNxHgLECA2EOMtQIDYQIy3AAFiAzHeAgSIDcR4CxAgNhDjLUCA2ECMtwABYgMx3gIEiA3EeAsQIDYQ4y1AgNhAjLcAAWIDMd4CBIgNxHgLECA2EOMtQIDYQIy3AAFiAzHeAgSIDcR4CxAgNhDjLUCA2ECMtwABYgMx3gIEiA3EeAsQIDYQ4y1AgNhAjLcAAWIDMd4C4gAPBr8Bkvi47jwAAAAASUVORK5CYII=" alt="image" width="128"></span></p>
            </td>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 0.25in;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">R: 3</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 0.25in;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">B: 115</span></p>
            </td>
        </tr>
        <tr>
            <td style="width: 106.5pt;border-color: currentcolor windowtext windowtext currentcolor;border-style: none solid solid none;border-width: medium 1pt 1pt medium;padding: 0in 5.4pt;height: 0.25in;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">G: 140</span></p>
            </td>
        </tr>
    </tbody>
</table>

## Step 3: Create basemap with color pallet.

I used the <a href="https://mapstyle.withgoogle.com/">Google Sytling Wizard</a> to create a custom basemap with colors pulled from my reference pallet table.

<img src="/gmap/ImageofMap.PNG" />

I also created a table that documented the colors changed for each section.

#### Colors Used For Map Features

<table style="border-collapse:collapse;border:none;">
    <tbody>
        <tr>
            <td style="width: 155.8pt; border: 1pt solid windowtext; padding: 0in 5.4pt; height: 21.1pt; vertical-align: top; text-align: center;"> <strong><span style="font-size:19px;">Feature Type</span></strong></td>
            <td style="width: 33.2339%; border-color: windowtext windowtext windowtext currentcolor; border-style: solid solid solid none; border-width: 1pt 1pt 1pt medium; border-image: none 100% / 1 / 0 stretch; padding: 0in 5.4pt; height: 21.1pt; vertical-align: top; text-align: center;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;text-align:center;'><strong><span style="font-size:19px;">Element Type</span></strong></p>
            </td>
            <td style="width: 33.2341%; border-color: windowtext windowtext windowtext currentcolor; border-style: solid solid solid none; border-width: 1pt 1pt 1pt medium; border-image: none 100% / 1 / 0 stretch; padding: 0in 5.4pt; height: 21.1pt; vertical-align: top; text-align: center;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;text-align:center;'><strong><span style="font-size:19px;">Styler</span></strong></p>
            </td>
        </tr>
        <tr>
            <td style="width: 155.8pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">All</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt; vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Geometry&nbsp;</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Mosque (#026873)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width: 155.8pt;border-color: currentcolor windowtext windowtext;border-style: none solid solid;border-width: medium 1pt 1pt;border-image: none 100% / 1 / 0 stretch;padding: 0in 5.4pt;vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">All</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt; vertical-align: top;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Labels</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Aubergine (#260911)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Landscape</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Geometry</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Mosque (#026873)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Administrative</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Geometry</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Wine Berry (#591830)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Administrative/Land parcel</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Stroke</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Cerulean (#04B2D9)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Administrative/Land parcel</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Labels/Text fill</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Aubergine (#260911)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Landscape/Natural</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Geometry</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt; vertical-align: top;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-size: 16px; font-family: Calibri, sans-serif;">Blue Lagoon (#03738C)</span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Points of Interest</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Geometry</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Stiletto (#8C264B)</span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Points of Interest</span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-size:16px;">Labels/Text Fill</span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Aubergine (#260911)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Park</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Stiletto (#8C264B)</span></span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Park</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Labels/Text Fill</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Aubergine (#260911)</span></span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Concrete (#F2F2F2)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road/Highway</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Carrot Orange (#F2911B)</span></span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road/Highway</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Stroke</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Korma (#8C6111)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road/Highway/Controlled area</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Carrot Orange (#F2911B)</span></span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road/Highway/Controlled area</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Stroke</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Korma (#8C6111)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road/Artery</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Concrete (#F2F2F2)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Road/Local</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Text fill</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Cioccolato (#59360A)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Transit/Line</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Brick Red (#BF3056)</span></span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Transit/Line</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Label/Text Fill</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt; vertical-align: top;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Wine Berry (#591830)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Transit/Line</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Label/Text Outline</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Concrete (#F2F2F2)</span></span></pre>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Transit/Station</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Stiletto (#8C264B)</span></span></p>
            </td>
        </tr>
        <tr>
            <td style="width:155.8pt;border:solid windowtext 1.0pt;border-top:  none;padding:0in 5.4pt 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Water</span></span></p>
            </td>
            <td style="width: 33.2339%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <p style='margin-top:0in;margin-right:0in;margin-bottom:0in;margin-left:0in;line-height:normal;font-size:15px;font-family:"Calibri",sans-serif;'><span style="font-family: Calibri, sans-serif;"><span style="font-size:16px;">Geometry</span></span></p>
            </td>
            <td style="width: 33.2341%; border-color: currentcolor windowtext windowtext currentcolor; border-style: none solid solid none; border-width: medium 1pt 1pt medium; padding: 0in 5.4pt;">
                <pre style='margin:0in;margin-bottom:.0001pt;font-size:13px;font-family:"Courier New";'><span style="font-family: Calibri, sans-serif;"><span style="font-size: 16px;">Brick Red (#BF3056)</span></span></pre>
            </td>
        </tr>
    </tbody>
</table>

## Export JSON, create API, and share the map.

I exported the JSON file containing the map color coding and created a Google Map API. Then, I used the API and reference code to create an interactive webpage version of the map.
           
[/gmap/google_map_example.html](Check out the interactive version of my custom Map Style for Global Links on the map page!)
            
