Former is a wrapper around a minimal web interface meant to provide interstitial web based interfaces to command line driven programs. You provide an HTML file in your loadpath that conforms to a couple of simple constraints, and Former takes care of spinning up a one-off server to host it on localhost, opening up your default browser, and even closing the window once the form is submitted.

Example usage:

 	survey = Former.new 'survey.html' # This call will set up a survey object, and prep the server to run
 	survey.run
 	survey			 # Survey now holds the parameters from survey.html as a hash
	
Currently, only single-page single-form templates are supported (and then, only in raw HTML). Support for HAML and multi-step forms is planned. 
