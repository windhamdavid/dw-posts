---
ID: 1331
post_title: wp_title() deprecated
author: David
post_date: 2015-10-27 16:17:04
post_excerpt: ""
layout: post
permalink: >
  https://davidawindham.com/wp_title-deprecated/
published: true
---
I had a bit of free time today to run some upgrades on my computer and see what's happening with this website. While doing so, I upgraded my localhost to WordPress 4.4 to test the new core-api features and I noticed that the <b>wp_title()</b> function is now throwing deprecated notices to the browser and log. ( e.g. <a href="https://make.wordpress.org/core/2015/10/20/document-title-in-4-4/">https://make.wordpress.org/core/2015/10/20/document-title-in-4-4/</a> )  I used to use a custom function for my page titles, but it's now handled by core in <b>wp_head()</b>. Since I know a lot of folks will be fishing for the answer on this once the upgrade is out, here's how I rewrote my theme <a href="https://github.com/windhamdavid/dw/blob/master/inc/template.php">template.php</a>. 

<pre data-language="php">
// ********* DEPRECATED wp_title() in 4.4 ***********
//if ( ! function_exists( 'dw_page_title') ) :
//function dw_page_title() {
//	global $page, $paged; 
//	wp_title( '|', true, 'right' ); 
//	bloginfo( 'name' ); $site_description = get_bloginfo( 'description', 'display' );
//	if ( $site_description && ( is_home() || is_front_page() ) )
//		echo " | $site_description";
//	if ( $paged >= 2 || $page >= 2 )
//		echo ' | ' . sprintf( __( 'Page %s', 'dw' ), max( $paged, $page ) );
//}
//endif;

function filter_wp_title( $title, $sep ) {
    global $paged, $page;
 
    if ( is_feed() )
        return $title;
 
    $title .= get_bloginfo( 'name' );
 
    $site_description = get_bloginfo( 'description', 'display' );
    if ( $site_description && ( is_home() || is_front_page() ) )
        $title = "$title $sep $site_description";

    if ( $paged >= 2 || $page >= 2 )
        $title = "$title $sep " . sprintf( __( 'Page %s', 'twentytwelve' ), max( $paged, $page ) );
 
    return $title;
}
add_filter( 'wp_title', 'filter_wp_title', 10, 2 );
add_filter( 'document_title_separator', function () { return '|'; } );
</pre>