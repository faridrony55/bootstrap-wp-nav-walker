+++++++++++++++
READ THIS FIRST
+++++++++++++++

THIS FUNCTION REQURIES THE BOOTSTRAP CSS AND JS FILES

1. ADD THE FOLLOWING LINES TO YOUR FUNCTIONS FILE. 

//START CODE/////////////////////////////////////////////////////////////////////////////////
//LOAD THE BOOTSTRAP CSS//

function front_styles() {  

	wp_register_style( 'latofont', 'http://fonts.googleapis.com/css?family=Lato');
	wp_enqueue_style( 'latofont' );

add_action( 'wp_enqueue_scripts', 'front_styles' );

//LOAD THE BOOTSTRAP JS//

function front_scripts() {  

    wp_enqueue_script( 'bootstrapjs', 'hhttp://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js', array('jquery'), '', true );

}
add_action( 'wp_enqueue_scripts', 'front_scripts' );

//END CODE/////////////////////////////////////////////////////////////////////////////////


2.

The sample HTML file is the basic right aligned menu and left aligned logo used in many websites. The actual PHP you can see
at the bottom with the call to the custom nav walker is the important part. 


3.

The function file is the file that controls the nav walker. Your better off copying whats in here and adding it to the bottom of yoru functions.php file in
your theme.