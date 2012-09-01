Ext.ux.panel.PDF
===============

A PDF Viewer Panel for the Sencha Touch 2 Framework - No Browser Plugin required, pure JavaScript.  
It renders one page at once because of rendering speed. The page scale can be changed by using multitouch gestures like the Zoom-Gesture or Pinch-To-Zoom.  
PDF Rendering is done using the great Mozilla PDF.js Library (<a href="https://github.com/mozilla/pdf.js">https://github.com/mozilla/pdf.js</a>).

By now the rendering speed isn´t very good. Take care by changing the maxPageScale config! I hope this is getting better with future development of mozilla´s PDF.JS.   
The rendered page looks a bit blurry. This can be fixed by applying a sharpening filter on the rendered canvas. But this will cost some more cpu time, because we cant use WebGL by now.

### Usage ###

    Ext.application({
    
        views : [
            'Ext.ux.panel.PDF'
        ],
        
        launch: function() {
            
            Ext.Viewport.add({
                xtype     : 'pdfpanel',
                fullscreen: true,
                layout    : 'fit',
                src       : 'http://cdn.mozilla.net/pdfjs/tracemonkey.pdf', // URL to the PDF - Same Domain or Server with CORS Support
            });
        }
    });
    
### Examples ###

For an demo, please visit <a href="http://SunboX.github.com/st2_pdf_panel/demo/SimpleViewer/">http://SunboX.github.com/st2_pdf_panel/demo/SimpleViewer/</a>  

Single page demo: <a href="http://SunboX.github.com/st2_pdf_panel/demo/NoToolbar/">http://SunboX.github.com/st2_pdf_panel/demo/NoToolbar/</a>  
