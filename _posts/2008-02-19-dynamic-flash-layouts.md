---
ID: 713
post_title: dynamic flash using ssp director
author: David
post_date: 2008-02-19 14:12:00
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/dynamic-flash-layouts/
published: true
---
<img src="http://davidawindham.com/images/ssp_array.png" alt="ssp array" />
<a href="http://davidawindham.com/org/ssp/"><img src="http://davidawindham.com/images/my_ssp.png" alt="slide show pro" /></a>
hey thanks.. <a href="http://www.imagemagick.org/script/index.php">imagemagick</a> and <a href="http://www.whatdoiknow.org/">todd dominey</a>..who actually did all of the really hard work on this one.. dominey knows what he's doing.. smart move licensing <a href="http://slideshowpro.net/products/slideshowpro_director/slideshowpro_director">director</a> per domain..it's worth it..i'll gladly pay for it.... and i can customize and use it now pretty seamlessly..almost anywhere to manage video, audio, text, html, and imagery.. including the entire layout and dynamic text /html with css attached inside of flash based pages.... which i would embed in this page (click image above for files) but it seams that <a href="http://kimili.com/plugins/kml_flashembed#faqs">kimili flash embed</a> won't support (bc the swf is dependent on other imported .swfs) an absolute src path from a url that is dynamic.. as this one is generated..... i'll have to work on this in the near future.. i'm just glad that i can now begin to build so many more dynamic sites using director to manage the media files, layout and text in swfs.
<a href="http://slideshowpro.net/products/slideshowpro_director/slideshowpro_director"><img src="http://davidawindham.com/images/sspdirector.png" alt="slide show pro director" /></a>
<img src="http://davidawindham.com/images/sspfla.png" alt="ssp fla" />
i'll add more parameters to it.. as i use it for other projects.. and thks in particular for the original array goes to <a href="http://www.shannon-jensen.com/">Shannon Jensen</a> a talented photographer as well.
<pre lang="actionscript" lineno="1">//modified from ssp user forums. http://slideshowpro.net by http://davidawindham.com
var totalImgs:Number;
var currentImgNumber:Number;
var theArr:Array;
var menublisten:Object = new Object;
menublisten.galleryData = function(eventObject):Void {
    theArr = eventObject.data;
    var menu_mc:MovieClip = _root.createEmptyMovieClip("menu_mc",350);
    var nexty:Number = 0;
    for (i=0; i<theArr.length; i++) {
        var mb:MovieClip = menu_mc.attachMovie("mb","mb_"+i,50+i, {_x:0,_y:nexty});
        mb.txt.text = theArr[i][0].title;
        nexty += mb._height;
        mb.onRelease = function() {
            var albumNum:Number = Number(this._name.split("_")[1]);
            ssp1.loadAlbum(albumNum);
			sspt1.loadAlbum(albumNum);
        }
    }
}
ssp1.addEventListener("galleryData", sspListener);

adata = new Object();
adata.onAlbumData = function(eventObject):Void {
	t_txt.html=true;
	t_txt.htmlText=eventObject.data.title;
	t2_txt.html=true;
	t2_txt.htmlText=eventObject.data.description;
	totalImgs = eventObject.data.totalImages;
}
ssp1.addEventListener("onAlbumData", adata);
sspt1.addEventListener("onAlbumData", adata);

idata = new Object();
idata.onImageData = function(eventObject):Void {
	t3_txt.html=true;
	t3_txt.htmlText=eventObject.data.caption;
	t4_txt.html=true;
	t4_txt.htmlText=eventObject.data.title;
	currentImgNumber = eventObject.data.number;
}
ssp1.addEventListener("onImageData", idata);
sspt1.addEventListener("onImageData", idata);

function nextImage() {
	if (currentImgNumber < totalImgs) {
		ssp1.nextImage();
		sspt1.nextImage();
	} else {
		ssp1.loadImageNumber(0);
		sspt1.loadImageNumber(0);
	}
}
function prevImage() {
	if (currentImgNumber >= 2) {
		ssp1.previousImage();
		sspt1.previousImage();
	} else {
		ssp1.loadImageNumber(totalImgs-1);
		sspt1.loadImageNumber(totalImgs-1);
	}
}
nextImage_bttn.onRelease = function() {
	nextImage();
}
nextImage_bttn2.onRelease = function() {
	nextImage();
}
prevImage_bttn.onRelease = function() {
	prevImage();
}
var stylie:TextField.StyleSheet = new TextField.StyleSheet();
stylie.onLoad = function(success:Boolean) {
	if (success) {
	//nada
	}
};

stylie.load("stylie.css");
t2_txt.styleSheet = stylie;
stop();
</pre>