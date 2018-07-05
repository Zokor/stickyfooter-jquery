# stickyfooter-jquery
Calculate when to put the footer sticky or not depending on the Header, Main and Footer height

function stickyFooter() {

    if (($(window).outerHeight() - $('header').outerHeight() - $('main').outerHeight() - $('footer').outerHeight()) > 0) {
      $('footer').addClass('sticky');
    } else {
      $('footer').removeClass('sticky');
    }

}

$(window).on('load', function () {
    stickyFooter();
});

$(window).resize(function () {
    stickyFooter();
});

