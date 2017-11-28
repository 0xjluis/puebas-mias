jQuery(document).ready(function(){
	var ancho_ventana = jQuery(window).width();
	scrollActivo = false;

	idExist = document.getElementById('contedor-img-envio')
	jQuery(window).scroll(moverImagen);

	if(ancho_ventana >= 768 && idExist){
		scrollActivo = true;
	}

	jQuery(window).resize(anchoVentana);
	jQuery(window).load(setMenuImg);


});

function setMenuImg (){
	var createImg1 = document.createElement("img");
	var createImg2 = document.createElement("img");
	var createImg3 = document.createElement("img");
	var createImg4 = document.createElement("img");
	var createImg5 = document.createElement("img");
	var createImg6 = document.createElement("img");

	createImg1.setAttribute("src","/themes/Himalia/img/kit-solar1.svg");
	createImg2.setAttribute("src","/themes/Himalia/img/panel-solar.svg");
	createImg3.setAttribute("src","/themes/Himalia/img/bateria.svg");
	createImg4.setAttribute("src","/themes/Himalia/img/regulador.svg");
	createImg5.setAttribute("src","/themes/Himalia/img/conversor.svg");
	createImg6.setAttribute("src","/themes/Himalia/img/estructura.svg");

	jQuery("#menu-kits-solares > a").prepend(createImg1);
	jQuery("#menu-paneles-solares > a").prepend(createImg2);
	jQuery("#menu-baterías- > a").prepend(createImg3);
	jQuery("#menu-reguladores-de-carga > a").prepend(createImg4);
	jQuery("#menu-inversores-solares > a").prepend(createImg5);
	jQuery("#menu-estructuras-paneles- > a").prepend(createImg6);

}

function anchoVentana(){
	ancho_nuevo = jQuery(window).width();

	if(ancho_nuevo >= 768 && idExist){
		scrollActivo = true;
	}else{
		scrollActivo = false;
	}
}

function moverImagen(){
	if(scrollActivo == true){
		var height = jQuery(window).scrollTop();

		if(height > jQuery("#contedor-img-envio").offset().top - 20)  {
	    	jQuery("#img-envio").addClass("img-envio-fixed");
	    } else {
	    	jQuery("#img-envio").removeClass("img-envio-fixed");
	    }

	    var texTop = jQuery(".tab-content").offset().top;
	    var texHeigth = jQuery(".tab-content").height();
	    var imgHeigth = jQuery("#img-envio").height();
	    var sumica = height + 20 + imgHeigth;
	    var columnsTop = jQuery("#columns").offset().top; 

	    if (height +  imgHeigth -19 >=  texHeigth + texTop ){
	    	jQuery("#img-envio").removeClass("img-envio-fixed");
	    	jQuery("#img-envio").addClass("img-envio-absolute")
	    	var topAbsolute = (texTop + texHeigth + 15) - (imgHeigth + columnsTop);
	    	jQuery("#img-envio").css("top",topAbsolute+"px");
		}else {
			jQuery("#img-envio").removeClass("img-envio-absolute")
	    	jQuery("#img-envio").css("top","none");
		}
	}else{
		jQuery("#img-envio").removeClass("img-envio-fixed");
		jQuery("#img-envio").removeClass("img-envio-absolute");
	}

}
