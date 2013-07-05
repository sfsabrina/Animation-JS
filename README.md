anime
=====

Animation JS inside background

var boat;

function boatmov() {
    var oldLeft = parseInt(boat.style.left) + boat.offsetWidth;

    var newLeft = ((oldLeft + 10) % (boat.parentElement.clientWidth + boat.offsetWidth)) - boat.offsetWidth;

    boat.style.left = newLeft + 'px';
}

function boatinit() {
    boat = document.getElementById('boat');

    boat.style.display = '';

    window.setInterval(boatmov, 250);
}
