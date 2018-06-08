
<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>Bike_Share_Analysis</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>

<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#login_widget {
  float: right;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: baseline;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
[dir="rtl"] #new-menu {
  text-align: right;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="2016-US-Bike-Share-Activity-Snapshot">2016 US Bike Share Activity Snapshot<a class="anchor-link" href="#2016-US-Bike-Share-Activity-Snapshot">&#182;</a></h1><h2 id="Table-of-Contents">Table of Contents<a class="anchor-link" href="#Table-of-Contents">&#182;</a></h2><ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#pose_questions">Posing Questions</a></li>
<li><a href="#wrangling">Data Collection and Wrangling</a><ul>
<li><a href="#condensing">Condensing the Trip Data</a></li>
</ul>
</li>
<li><a href="#eda">Exploratory Data Analysis</a><ul>
<li><a href="#statistics">Statistics</a></li>
<li><a href="#visualizations">Visualizations</a></li>
</ul>
</li>
<li><a href="#eda_continued">Performing Your Own Analysis</a></li>
<li><a href="#conclusions">Conclusions</a></li>
</ul>
<p><a id='intro'></a></p>
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><blockquote><p><strong>Tip</strong>: Quoted sections like this will provide helpful instructions on how to navigate and use a Jupyter notebook.</p>
</blockquote>
<p>Over the past decade, bicycle-sharing systems have been growing in number and popularity in cities across the world. Bicycle-sharing systems allow users to rent bicycles for short trips, typically 30 minutes or less. Thanks to the rise in information technologies, it is easy for a user of the system to access a dock within the system to unlock or return bicycles. These technologies also provide a wealth of data that can be used to explore how these bike-sharing systems are used.</p>
<p>In this project, you will perform an exploratory analysis on data provided by <a href="https://www.motivateco.com/">Motivate</a>, a bike-share system provider for many major cities in the United States. You will compare the system usage between three large cities: New York City, Chicago, and Washington, DC. You will also see if there are any differences within each system for those users that are registered, regular users and those users that are short-term, casual users.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='pose_questions'></a></p>
<h2 id="Posing-Questions">Posing Questions<a class="anchor-link" href="#Posing-Questions">&#182;</a></h2><p>Before looking at the bike sharing data, you should start by asking questions you might want to understand about the bike share data. Consider, for example, if you were working for Motivate. What kinds of information would you want to know about in order to make smarter business decisions? If you were a user of the bike-share service, what factors might influence how you would want to use the service?</p>
<p><strong>Question 1</strong>: Write at least two questions related to bike sharing that you think could be answered by data.</p>
<p><strong>Answer</strong>: 1. how many users are using my service in a particular region/city?</p>

<pre><code>        2. what is the peak time ie) At what time, more people are  using my service?
        3. How many repetitve customers?
        4. in one month how many distance people are travelling (cummlative) using my service ?
        5. What are all the different types of services they are providing so that i can select the one that is suitable for                me? 
        6. Is the service easily accessible? ie) do i have to travel far to avail the service 
        7. If i didnt like the service. will they refund or find a solution immeditaely ?

</code></pre>
<blockquote><p><strong>Tip</strong>: If you double click on this cell, you will see the text change so that all of the formatting is removed. This allows you to edit this block of text. This block of text is written using <a href="http://daringfireball.net/projects/markdown/syntax">Markdown</a>, which is a way to format text using headers, links, italics, and many other options using a plain-text syntax. You will also use Markdown later in the Nanodegree program. Use <strong>Shift</strong> + <strong>Enter</strong> or <strong>Shift</strong> + <strong>Return</strong> to run the cell and show its rendered form.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='wrangling'></a></p>
<h2 id="Data-Collection-and-Wrangling">Data Collection and Wrangling<a class="anchor-link" href="#Data-Collection-and-Wrangling">&#182;</a></h2><p>Now it's time to collect and explore our data. In this project, we will focus on the record of individual trips taken in 2016 from our selected cities: New York City, Chicago, and Washington, DC. Each of these cities has a page where we can freely download the trip data.:</p>
<ul>
<li>New York City (Citi Bike): <a href="https://www.citibikenyc.com/system-data">Link</a></li>
<li>Chicago (Divvy): <a href="https://www.divvybikes.com/system-data">Link</a></li>
<li>Washington, DC (Capital Bikeshare): <a href="https://www.capitalbikeshare.com/system-data">Link</a></li>
</ul>
<p>If you visit these pages, you will notice that each city has a different way of delivering its data. Chicago updates with new data twice a year, Washington DC is quarterly, and New York City is monthly. <strong>However, you do not need to download the data yourself.</strong> The data has already been collected for you in the <code>/data/</code> folder of the project files. While the original data for 2016 is spread among multiple files for each city, the files in the <code>/data/</code> folder collect all of the trip data for the year into one file per city. Some data wrangling of inconsistencies in timestamp format within each city has already been performed for you. In addition, a random 2% sample of the original data is taken to make the exploration more manageable.</p>
<p><strong>Question 2</strong>: However, there is still a lot of data for us to investigate, so it's a good idea to start off by looking at one entry from each of the cities we're going to analyze. Run the first code cell below to load some packages and functions that you'll be using in your analysis. Then, complete the second code cell to print out the first trip recorded from each of the cities (the second line of each data file).</p>
<blockquote><p><strong>Tip</strong>: You can run a code cell like you formatted Markdown cells above by clicking on the cell and using the keyboard shortcut <strong>Shift</strong> + <strong>Enter</strong> or <strong>Shift</strong> + <strong>Return</strong>. Alternatively, a code cell can be executed using the <strong>Play</strong> button in the toolbar after selecting it. While the cell is running, you will see an asterisk in the message to the left of the cell, i.e. <code>In [*]:</code>. The asterisk will change into a number to show that execution has completed, e.g. <code>In [1]</code>. If there is output, it will show up as <code>Out [1]:</code>, with an appropriate number to match the "In" number.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[55]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## import all necessary packages and functions.</span>
<span class="kn">import</span> <span class="nn">csv</span> <span class="c1"># read and write csv files</span>
<span class="kn">from</span> <span class="nn">datetime</span> <span class="k">import</span> <span class="n">datetime</span> <span class="c1"># operations to parse dates</span>
<span class="kn">from</span> <span class="nn">pprint</span> <span class="k">import</span> <span class="n">pprint</span> <span class="c1"># use to print data structures like dictionaries in</span>
                          <span class="c1"># a nicer way than the base print function.</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[57]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">print_first_point</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function prints and returns the first data point (second row) from</span>
<span class="sd">    a csv file that includes a header row.</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="c1"># print city name for reference</span>
    <span class="n">city</span> <span class="o">=</span> <span class="n">filename</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39;-&#39;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s1">&#39;/&#39;</span><span class="p">)[</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;</span><span class="se">\n</span><span class="s1">City: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">city</span><span class="p">))</span>
    
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1">## TODO: Use the csv library to set up a DictReader object. ##</span>
        <span class="c1">## see https://docs.python.org/3/library/csv.html           ##</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
    
        
        <span class="c1">## TODO: Use a function on the DictReader object to read the     ##</span>
        <span class="c1">## first trip from the data file and store it in a variable.     ##</span>
        <span class="c1">## see https://docs.python.org/3/library/csv.html#reader-objects ##</span>
        <span class="n">first_trip</span> <span class="o">=</span> <span class="n">trip_reader</span><span class="o">.</span><span class="fm">__next__</span><span class="p">()</span>
        

        
        
        <span class="c1">## TODO: Use the pprint library to print the first trip. ##</span>
        <span class="n">pprint</span><span class="p">(</span><span class="n">first_trip</span><span class="p">)</span>
        <span class="c1">## see https://docs.python.org/3/library/pprint.html     ##</span>
        
    <span class="c1"># output city name and first trip for later testing</span>
    <span class="k">return</span> <span class="p">(</span><span class="n">city</span><span class="p">,</span> <span class="n">first_trip</span><span class="p">)</span>

<span class="c1"># list of files for each city</span>
<span class="n">data_files</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;./data/NYC-CitiBike-2016.csv&#39;</span><span class="p">,</span>
              <span class="s1">&#39;./data/Chicago-Divvy-2016.csv&#39;</span><span class="p">,</span>
              <span class="s1">&#39;./data/Washington-CapitalBikeshare-2016.csv&#39;</span><span class="p">,]</span>

<span class="c1"># print the first trip from each file, store in dictionary</span>
<span class="n">example_trips</span> <span class="o">=</span> <span class="p">{}</span>
<span class="k">for</span> <span class="n">data_file</span> <span class="ow">in</span> <span class="n">data_files</span><span class="p">:</span>
    <span class="n">city</span><span class="p">,</span> <span class="n">first_trip</span> <span class="o">=</span> <span class="n">print_first_point</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
    <span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">]</span> <span class="o">=</span> <span class="n">first_trip</span>
    
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>
City: NYC
OrderedDict([(&#39;tripduration&#39;, &#39;839&#39;),
             (&#39;starttime&#39;, &#39;1/1/2016 00:09:55&#39;),
             (&#39;stoptime&#39;, &#39;1/1/2016 00:23:54&#39;),
             (&#39;start station id&#39;, &#39;532&#39;),
             (&#39;start station name&#39;, &#39;S 5 Pl &amp; S 4 St&#39;),
             (&#39;start station latitude&#39;, &#39;40.710451&#39;),
             (&#39;start station longitude&#39;, &#39;-73.960876&#39;),
             (&#39;end station id&#39;, &#39;401&#39;),
             (&#39;end station name&#39;, &#39;Allen St &amp; Rivington St&#39;),
             (&#39;end station latitude&#39;, &#39;40.72019576&#39;),
             (&#39;end station longitude&#39;, &#39;-73.98997825&#39;),
             (&#39;bikeid&#39;, &#39;17109&#39;),
             (&#39;usertype&#39;, &#39;Customer&#39;),
             (&#39;birth year&#39;, &#39;&#39;),
             (&#39;gender&#39;, &#39;0&#39;)])

City: Chicago
OrderedDict([(&#39;trip_id&#39;, &#39;9080545&#39;),
             (&#39;starttime&#39;, &#39;3/31/2016 23:30&#39;),
             (&#39;stoptime&#39;, &#39;3/31/2016 23:46&#39;),
             (&#39;bikeid&#39;, &#39;2295&#39;),
             (&#39;tripduration&#39;, &#39;926&#39;),
             (&#39;from_station_id&#39;, &#39;156&#39;),
             (&#39;from_station_name&#39;, &#39;Clark St &amp; Wellington Ave&#39;),
             (&#39;to_station_id&#39;, &#39;166&#39;),
             (&#39;to_station_name&#39;, &#39;Ashland Ave &amp; Wrightwood Ave&#39;),
             (&#39;usertype&#39;, &#39;Subscriber&#39;),
             (&#39;gender&#39;, &#39;Male&#39;),
             (&#39;birthyear&#39;, &#39;1990&#39;)])

City: Washington
OrderedDict([(&#39;Duration (ms)&#39;, &#39;427387&#39;),
             (&#39;Start date&#39;, &#39;3/31/2016 22:57&#39;),
             (&#39;End date&#39;, &#39;3/31/2016 23:04&#39;),
             (&#39;Start station number&#39;, &#39;31602&#39;),
             (&#39;Start station&#39;, &#39;Park Rd &amp; Holmead Pl NW&#39;),
             (&#39;End station number&#39;, &#39;31207&#39;),
             (&#39;End station&#39;, &#39;Georgia Ave and Fairmont St NW&#39;),
             (&#39;Bike number&#39;, &#39;W20842&#39;),
             (&#39;Member Type&#39;, &#39;Registered&#39;)])
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>If everything has been filled out correctly, you should see below the printout of each city name (which has been parsed from the data file name) that the first trip has been parsed in the form of a dictionary. When you set up a <code>DictReader</code> object, the first row of the data file is normally interpreted as column names. Every other row in the data file will use those column names as keys, as a dictionary is generated for each row.</p>
<p>This will be useful since we can refer to quantities by an easily-understandable label instead of just a numeric index. For example, if we have a trip stored in the variable <code>row</code>, then we would rather get the trip duration from <code>row['duration']</code> instead of <code>row[0]</code>.</p>
<p><a id='condensing'></a></p>
<h3 id="Condensing-the-Trip-Data">Condensing the Trip Data<a class="anchor-link" href="#Condensing-the-Trip-Data">&#182;</a></h3><p>It should also be observable from the above printout that each city provides different information. Even where the information is the same, the column names and formats are sometimes different. To make things as simple as possible when we get to the actual exploration, we should trim and clean the data. Cleaning the data makes sure that the data formats across the cities are consistent, while trimming focuses only on the parts of the data we are most interested in to make the exploration easier to work with.</p>
<p>You will generate new data files with five values of interest for each trip: trip duration, starting month, starting hour, day of the week, and user type. Each of these may require additional wrangling depending on the city:</p>
<ul>
<li><strong>Duration</strong>: This has been given to us in seconds (New York, Chicago) or milliseconds (Washington). A more natural unit of analysis will be if all the trip durations are given in terms of minutes.</li>
<li><strong>Month</strong>, <strong>Hour</strong>, <strong>Day of Week</strong>: Ridership volume is likely to change based on the season, time of day, and whether it is a weekday or weekend. Use the start time of the trip to obtain these values. The New York City data includes the seconds in their timestamps, while Washington and Chicago do not. The <a href="https://docs.python.org/3/library/datetime.html"><code>datetime</code></a> package will be very useful here to make the needed conversions.</li>
<li><strong>User Type</strong>: It is possible that users who are subscribed to a bike-share system will have different patterns of use compared to users who only have temporary passes. Washington divides its users into two types: 'Registered' for users with annual, monthly, and other longer-term subscriptions, and 'Casual', for users with 24-hour, 3-day, and other short-term passes. The New York and Chicago data uses 'Subscriber' and 'Customer' for these groups, respectively. For consistency, you will convert the Washington labels to match the other two.</li>
</ul>
<p><strong>Question 3a</strong>: Complete the helper functions in the code cells below to address each of the cleaning tasks described above.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[58]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">duration_in_mins</span><span class="p">(</span><span class="n">datum</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    Takes as input a dictionary containing info about a single trip (datum) and</span>
<span class="sd">    its origin city (city) and returns the trip duration in units of minutes.</span>
<span class="sd">    </span>
<span class="sd">    Remember that Washington is in terms of milliseconds while Chicago and NYC</span>
<span class="sd">    are in terms of seconds. </span>
<span class="sd">    </span>
<span class="sd">    HINT: The csv module reads in all of the data as strings, including numeric</span>
<span class="sd">    values. You will need a function to convert the strings into an appropriate</span>
<span class="sd">    numeric type when making your transformations.</span>
<span class="sd">    see https://docs.python.org/3/library/functions.html</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="c1"># YOUR CODE HERE</span>
  
    <span class="k">if</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;NYC&#39;</span> <span class="ow">or</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span>
        <span class="n">trip_dur</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;tripduration&#39;</span><span class="p">])</span>
        <span class="n">duration</span> <span class="o">=</span> <span class="p">(</span><span class="n">trip_dur</span> <span class="o">/</span> <span class="mi">60</span><span class="p">)</span>
        
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span><span class="p">:</span>
        <span class="n">trip_dur_was</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Duration (ms)&#39;</span><span class="p">])</span>
        
        <span class="n">duration</span> <span class="o">=</span> <span class="p">(</span><span class="n">trip_dur_was</span><span class="o">/</span><span class="p">(</span><span class="mi">1000</span><span class="o">*</span><span class="mi">60</span><span class="p">))</span>
        
        
        
        
    
        
   
    <span class="k">return</span> <span class="n">duration</span>


<span class="c1"># Some tests to check that your code works. There should be no output if all of</span>
<span class="c1"># the assertions pass. The `example_trips` dictionary was obtained from when</span>
<span class="c1"># you printed the first trip from each of the original data files.</span>
<span class="n">tests</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="mf">13.9833</span><span class="p">,</span>
         <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="mf">15.4333</span><span class="p">,</span>
         <span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="mf">7.1231</span><span class="p">}</span>

<span class="k">for</span> <span class="n">city</span> <span class="ow">in</span> <span class="n">tests</span><span class="p">:</span>
    <span class="k">assert</span> <span class="nb">abs</span><span class="p">(</span><span class="n">duration_in_mins</span><span class="p">(</span><span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span> <span class="o">-</span> <span class="n">tests</span><span class="p">[</span><span class="n">city</span><span class="p">])</span> <span class="o">&lt;</span> <span class="o">.</span><span class="mi">001</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[63]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">type_of_user</span><span class="p">(</span><span class="n">datum</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    Takes as input a dictionary containing info about a single trip (datum) and</span>
<span class="sd">    its origin city (city) and returns the type of system user that made the</span>
<span class="sd">    trip.</span>
<span class="sd">    </span>
<span class="sd">    Remember that Washington has different category names compared to Chicago</span>
<span class="sd">    and NYC. </span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="k">global</span> <span class="n">user_type</span>
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">if</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;NYC&#39;</span> <span class="ow">or</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span>
        <span class="n">user_type</span> <span class="o">=</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;usertype&#39;</span><span class="p">]</span>
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span> <span class="ow">and</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Registered&#39;</span><span class="p">:</span>
        <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="s1">&#39;Subscriber&#39;</span>
        <span class="n">user_type</span> <span class="o">=</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span>
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span> <span class="ow">and</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Casual&#39;</span><span class="p">:</span>
        <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="s1">&#39;Customer&#39;</span>
        <span class="n">user_type</span> <span class="o">=</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Member Type&#39;</span><span class="p">]</span> 
    
    <span class="k">return</span> <span class="n">user_type</span>


<span class="c1"># Some tests to check that your code works. There should be no output if all of</span>
<span class="c1"># the assertions pass. The `example_trips` dictionary was obtained from when</span>
<span class="c1"># you printed the first trip from each of the original data files.</span>
<span class="n">tests</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="s1">&#39;Customer&#39;</span><span class="p">,</span>
         <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">,</span>
         <span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">}</span>

<span class="k">for</span> <span class="n">city</span> <span class="ow">in</span> <span class="n">tests</span><span class="p">:</span>
    <span class="k">assert</span> <span class="n">type_of_user</span><span class="p">(</span><span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span> <span class="o">==</span> <span class="n">tests</span><span class="p">[</span><span class="n">city</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[60]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">time_of_trip</span><span class="p">(</span><span class="n">datum</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    Takes as input a dictionary containing info about a single trip (datum) and</span>
<span class="sd">    its origin city (city) and returns the month, hour, and day of the week in</span>
<span class="sd">    which the trip was made.</span>
<span class="sd">    </span>
<span class="sd">    Remember that NYC includes seconds, while Washington and Chicago do not.</span>
<span class="sd">    </span>
<span class="sd">    HINT: You should use the datetime module to parse the original date</span>
<span class="sd">    strings into a format that is useful for extracting the desired information.</span>
<span class="sd">    see https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior</span>
<span class="sd">    &quot;&quot;&quot;</span>
    
    <span class="c1"># YOUR CODE HERE</span>
    <span class="k">if</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;NYC&#39;</span><span class="p">:</span>
        <span class="n">t</span> <span class="o">=</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">]</span>
        <span class="n">mymonth</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">t</span><span class="p">,</span><span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M:%S&#39;</span><span class="p">)</span>
        <span class="n">month</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%-m&#39;</span><span class="p">))</span>
        <span class="n">hour</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%-H&#39;</span><span class="p">))</span>
        <span class="n">day_of_week</span> <span class="o">=</span> <span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%A&#39;</span><span class="p">)</span>
        <span class="c1">#print(month,hour,day_of_week)</span>
    
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span>
        <span class="n">t</span> <span class="o">=</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">]</span>
        <span class="n">mymonth</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">t</span><span class="p">,</span><span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
        <span class="n">month</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%-m&#39;</span><span class="p">))</span>
        <span class="n">hour</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%-H&#39;</span><span class="p">))</span>
        <span class="n">day_of_week</span> <span class="o">=</span> <span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%A&#39;</span><span class="p">)</span>
        <span class="c1">#print(month,hour,day_of_week)</span>
        
    <span class="k">elif</span> <span class="n">city</span> <span class="o">==</span> <span class="s1">&#39;Washington&#39;</span><span class="p">:</span>
        <span class="n">t</span> <span class="o">=</span> <span class="n">datum</span><span class="p">[</span><span class="s1">&#39;Start date&#39;</span><span class="p">]</span>
        <span class="n">mymonth</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">t</span><span class="p">,</span><span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
        <span class="n">month</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%-m&#39;</span><span class="p">))</span>
        <span class="n">hour</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%-H&#39;</span><span class="p">))</span>
        <span class="n">day_of_week</span> <span class="o">=</span> <span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%A&#39;</span><span class="p">)</span>
        <span class="c1">#print(month,hour,day_of_week)</span>
    
    
    <span class="k">return</span> <span class="p">(</span><span class="n">month</span><span class="p">,</span> <span class="n">hour</span><span class="p">,</span> <span class="n">day_of_week</span><span class="p">)</span>


<span class="c1"># Some tests to check that your code works. There should be no output if all of</span>
<span class="c1"># the assertions pass. The `example_trips` dictionary was obtained from when</span>
<span class="c1"># you printed the first trip from each of the original data files.</span>
<span class="n">tests</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">0</span><span class="p">,</span> <span class="s1">&#39;Friday&#39;</span><span class="p">),</span>
         <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">23</span><span class="p">,</span> <span class="s1">&#39;Thursday&#39;</span><span class="p">),</span>
         <span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">3</span><span class="p">,</span> <span class="mi">22</span><span class="p">,</span> <span class="s1">&#39;Thursday&#39;</span><span class="p">)}</span>

<span class="k">for</span> <span class="n">city</span> <span class="ow">in</span> <span class="n">tests</span><span class="p">:</span>
    <span class="k">assert</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">example_trips</span><span class="p">[</span><span class="n">city</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span> <span class="o">==</span> <span class="n">tests</span><span class="p">[</span><span class="n">city</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Question 3b</strong>: Now, use the helper functions you wrote above to create a condensed data file for each city consisting only of the data fields indicated above. In the <code>/examples/</code> folder, you will see an example datafile from the <a href="http://www.bayareabikeshare.com/open-data">Bay Area Bike Share</a> before and after conversion. Make sure that your output is formatted to be consistent with the example file.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[20]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">condense_data</span><span class="p">(</span><span class="n">in_file</span><span class="p">,</span> <span class="n">out_file</span><span class="p">,</span> <span class="n">city</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function takes full data from the specified input file</span>
<span class="sd">    and writes the condensed data to a specified output file. The city</span>
<span class="sd">    argument determines how the input file will be parsed.</span>
<span class="sd">    </span>
<span class="sd">    HINT: See the cell below to see how the arguments are structured!</span>
<span class="sd">    &quot;&quot;&quot;</span>
    
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">out_file</span><span class="p">,</span> <span class="s1">&#39;w&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_out</span><span class="p">,</span> <span class="nb">open</span><span class="p">(</span><span class="n">in_file</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv DictWriter object - writer requires column names for the</span>
        <span class="c1"># first row as the &quot;fieldnames&quot; argument</span>
        <span class="n">out_colnames</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">,</span> <span class="s1">&#39;month&#39;</span><span class="p">,</span> <span class="s1">&#39;hour&#39;</span><span class="p">,</span> <span class="s1">&#39;day_of_week&#39;</span><span class="p">,</span> <span class="s1">&#39;user_type&#39;</span><span class="p">]</span>        
        <span class="n">trip_writer</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictWriter</span><span class="p">(</span><span class="n">f_out</span><span class="p">,</span> <span class="n">fieldnames</span> <span class="o">=</span> <span class="n">out_colnames</span><span class="p">)</span>
        <span class="n">trip_writer</span><span class="o">.</span><span class="n">writeheader</span><span class="p">()</span>
        <span class="c1">## TODO: set up csv DictReader object ##</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        <span class="c1"># collect data from and process each row</span>
        <span class="n">temp</span> <span class="o">=</span> <span class="p">[]</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="c1">#print(row)</span>
            <span class="c1"># set up a dictionary to hold the values for the cleaned and trimmed</span>
            <span class="c1"># data point</span>
            <span class="n">new_point</span> <span class="o">=</span> <span class="p">{}</span>
            <span class="c1">## TODO: use the helper functions to get the cleaned data from  ##</span>
            <span class="c1">## the original data dictionaries.                              ##</span>
            <span class="c1">## Note that the keys for the new_point dictionary should match ##</span>
            <span class="c1">## the column names set in the DictWriter object above.         ##</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">duration_in_mins</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            
            <span class="n">month</span><span class="p">,</span><span class="n">hour</span><span class="p">,</span><span class="n">day_of_week</span> <span class="o">=</span> <span class="n">time_of_trip</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;month&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">month</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;hour&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">hour</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;day_of_week&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">day_of_week</span>
            <span class="n">new_point</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">type_of_user</span><span class="p">(</span><span class="n">row</span><span class="p">,</span> <span class="n">city</span><span class="p">)</span>
            <span class="c1">## TODO: write the processed information to the output file.     ##</span>
                <span class="c1">## see https://docs.python.org/3/library/csv.html#writer-objects #</span>
            <span class="c1">#print(new_point)</span>
            <span class="c1">#temp.append(new_point)</span>
        <span class="c1">#print(temp)</span>
            <span class="c1">#new_point = new_point</span>
            <span class="n">trip_writer</span><span class="o">.</span><span class="n">writerow</span><span class="p">(</span><span class="n">new_point</span><span class="p">)</span>
            
    

                
    
        
            
     
            
           
            
            
            
            
       
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[21]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Run this cell to check your work</span>
<span class="n">city_info</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;Washington&#39;</span><span class="p">:</span> <span class="p">{</span><span class="s1">&#39;in_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Washington-CapitalBikeshare-2016.csv&#39;</span><span class="p">,</span>
                            <span class="s1">&#39;out_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span><span class="p">},</span>
             <span class="s1">&#39;Chicago&#39;</span><span class="p">:</span> <span class="p">{</span><span class="s1">&#39;in_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Chicago-Divvy-2016.csv&#39;</span><span class="p">,</span>
                         <span class="s1">&#39;out_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span><span class="p">},</span>
             <span class="s1">&#39;NYC&#39;</span><span class="p">:</span> <span class="p">{</span><span class="s1">&#39;in_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/NYC-CitiBike-2016.csv&#39;</span><span class="p">,</span>
                     <span class="s1">&#39;out_file&#39;</span><span class="p">:</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span><span class="p">}}</span>

<span class="k">for</span> <span class="n">city</span><span class="p">,</span> <span class="n">filenames</span> <span class="ow">in</span> <span class="n">city_info</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="n">condense_data</span><span class="p">(</span><span class="n">filenames</span><span class="p">[</span><span class="s1">&#39;in_file&#39;</span><span class="p">],</span> <span class="n">filenames</span><span class="p">[</span><span class="s1">&#39;out_file&#39;</span><span class="p">],</span> <span class="n">city</span><span class="p">)</span>
    <span class="n">print_first_point</span><span class="p">(</span><span class="n">filenames</span><span class="p">[</span><span class="s1">&#39;out_file&#39;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>
City: Washington
OrderedDict([(&#39;duration&#39;, &#39;7.123116666666666&#39;),
             (&#39;month&#39;, &#39;3&#39;),
             (&#39;hour&#39;, &#39;22&#39;),
             (&#39;day_of_week&#39;, &#39;Thursday&#39;),
             (&#39;user_type&#39;, &#39;Subscriber&#39;)])

City: Chicago
OrderedDict([(&#39;duration&#39;, &#39;15.433333333333334&#39;),
             (&#39;month&#39;, &#39;3&#39;),
             (&#39;hour&#39;, &#39;23&#39;),
             (&#39;day_of_week&#39;, &#39;Thursday&#39;),
             (&#39;user_type&#39;, &#39;Subscriber&#39;)])

City: NYC
OrderedDict([(&#39;duration&#39;, &#39;13.983333333333333&#39;),
             (&#39;month&#39;, &#39;1&#39;),
             (&#39;hour&#39;, &#39;0&#39;),
             (&#39;day_of_week&#39;, &#39;Friday&#39;),
             (&#39;user_type&#39;, &#39;Customer&#39;)])
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><p><strong>Tip</strong>: If you save a jupyter Notebook, the output from running code blocks will also be saved. However, the state of your workspace will be reset once a new session is started. Make sure that you run all of the necessary code blocks from your previous session to reestablish variables and functions before picking up where you last left off.</p>
</blockquote>
<p><a id='eda'></a></p>
<h2 id="Exploratory-Data-Analysis">Exploratory Data Analysis<a class="anchor-link" href="#Exploratory-Data-Analysis">&#182;</a></h2><p>Now that you have the data collected and wrangled, you're ready to start exploring the data. In this section you will write some code to compute descriptive statistics from the data. You will also be introduced to the <code>matplotlib</code> library to create some basic histograms of the data.</p>
<p><a id='statistics'></a></p>
<h3 id="Statistics">Statistics<a class="anchor-link" href="#Statistics">&#182;</a></h3><p>First, let's compute some basic counts. The first cell below contains a function that uses the csv module to iterate through a provided data file, returning the number of trips made by subscribers and customers. The second cell runs this function on the example Bay Area data in the <code>/examples/</code> folder. Modify the cells to answer the question below.</p>
<p><strong>Question 4a</strong>: Which city has the highest number of trips? Which city has the highest proportion of trips made by subscribers? Which city has the highest proportion of trips made by short-term customers?</p>
<p><strong>Answer</strong>:</p>
<p>highest number of trips: NYC
The highest propotion of subscribers recorded in nyc: 0.89
highest proportion of trips made by short-term customers: Chicago</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[22]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">trips_cities</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>        
        <span class="n">n</span> <span class="o">=</span> <span class="mi">0</span>        
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="n">n</span> <span class="o">+=</span><span class="mi">1</span>
        <span class="k">return</span> <span class="n">n</span>
    
<span class="k">def</span> <span class="nf">high_trips</span><span class="p">(</span><span class="n">city</span><span class="p">):</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="n">data_files_c</span> <span class="o">=</span>  <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span>
    <span class="n">data_files_w</span> <span class="o">=</span>  <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span>
    
    <span class="n">chicago</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="c1">#print(chicago)</span>
    <span class="n">nyc</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="c1">#print(nyc)</span>
    <span class="n">washington</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    <span class="c1">#print(washington)</span>
    
    <span class="k">if</span> <span class="n">chicago</span> <span class="o">&gt;</span> <span class="n">nyc</span> <span class="ow">and</span> <span class="n">chicago</span> <span class="o">&gt;</span> <span class="n">washington</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest no. of trips recorded in chicago: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">chicago</span><span class="p">)</span>
    <span class="k">elif</span> <span class="n">nyc</span> <span class="o">&gt;</span> <span class="n">washington</span> <span class="ow">and</span> <span class="n">nyc</span> <span class="o">&gt;</span> <span class="n">chicago</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest no. of trips recorded in nyc: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">nyc</span><span class="p">)</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest no. of trips recorded in washington: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">washington</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">high_trips</span><span class="p">(</span><span class="n">city</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The highest no. of trips recorded in nyc: 276798
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[23]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## Modify this and the previous cell to answer Question 4a. Remember to run ##</span>
<span class="c1">## the function on the cleaned data files you created from Question 3.      ##</span>

<span class="k">def</span> <span class="nf">number_of_customers</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function reads in a file with trip data and reports the number of</span>
<span class="sd">    trips made by subscribers, customers, and total overall.</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv reader object</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="n">n_customers</span> <span class="o">=</span> <span class="mi">0</span>
        
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Customer&#39;</span><span class="p">:</span>
                <span class="n">n_customers</span> <span class="o">+=</span> <span class="mi">1</span>
                
        <span class="k">return</span> <span class="n">n_customers</span>
                
<span class="k">def</span> <span class="nf">customer_propotion</span><span class="p">(</span><span class="n">data_file</span><span class="p">):</span>
    <span class="n">data_file</span> <span class="o">=</span> <span class="s1">&#39;./examples/BayArea-Y3-Summary.csv&#39;</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="n">data_files_c</span> <span class="o">=</span>  <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span>
    <span class="n">data_files_w</span> <span class="o">=</span>  <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span>
    
    <span class="n">chicago</span> <span class="o">=</span> <span class="n">number_of_customers</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="c1">#print(chicago)</span>
    <span class="n">nyc</span> <span class="o">=</span> <span class="n">number_of_customers</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="c1">#print(nyc)</span>
    <span class="n">washington</span> <span class="o">=</span> <span class="n">number_of_customers</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    <span class="c1">#print(washington)</span>
    
    <span class="n">tot_trip_c</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="n">tot_trip_n</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="n">tot_trip_w</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    
    <span class="n">chicago_prop</span> <span class="o">=</span> <span class="n">chicago</span> <span class="o">/</span> <span class="n">tot_trip_c</span>
    <span class="n">nyc_prop</span> <span class="o">=</span> <span class="n">nyc</span> <span class="o">/</span> <span class="n">tot_trip_n</span>
    <span class="n">washington_prop</span> <span class="o">=</span> <span class="n">washington</span> <span class="o">/</span> <span class="n">tot_trip_w</span>
    
    <span class="k">if</span> <span class="n">chicago_prop</span> <span class="o">&gt;</span> <span class="n">nyc_prop</span> <span class="ow">and</span> <span class="n">chicago_prop</span> <span class="o">&gt;</span> <span class="n">washington_prop</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest propotion of customers recorded in chicago: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="nb">round</span><span class="p">(</span><span class="n">chicago_prop</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>
    <span class="k">elif</span> <span class="n">nyc_prop</span> <span class="o">&gt;</span> <span class="n">washington_prop</span> <span class="ow">and</span> <span class="n">nyc_prop</span> <span class="o">&gt;</span> <span class="n">chicago_prop</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest propotion of customers recorded in nyc: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="nb">round</span><span class="p">(</span><span class="n">nyc_prop</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest propotion of customers recorded in washington: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="nb">round</span><span class="p">(</span><span class="n">washington_prop</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>

<span class="nb">print</span><span class="p">(</span><span class="n">customer_propotion</span><span class="p">(</span><span class="n">data_file</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The highest propotion of customers recorded in chicago: 0.24
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[25]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">number_of_subscribers</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="sd">&quot;&quot;&quot;</span>
<span class="sd">    This function reads in a file with trip data and reports the number of</span>
<span class="sd">    trips made by subscribers, customers, and total overall.</span>
<span class="sd">    &quot;&quot;&quot;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span> <span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f_in</span><span class="p">:</span>
        <span class="c1"># set up csv reader object</span>
        <span class="n">reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f_in</span><span class="p">)</span>
        
        <span class="c1"># initialize count variables</span>
        <span class="n">n_subscribers</span> <span class="o">=</span> <span class="mi">0</span>
        <span class="c1">#n_customers = 0</span>
        
        <span class="c1"># tally up ride types</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">n_subscribers</span> <span class="o">+=</span> <span class="mi">1</span>
        <span class="k">return</span> <span class="n">n_subscribers</span>
    
<span class="k">def</span> <span class="nf">propotion</span><span class="p">(</span><span class="n">subscribers</span><span class="p">):</span>
    <span class="n">subscribers</span> <span class="o">=</span> <span class="kc">None</span>
    <span class="n">data_file</span> <span class="o">=</span> <span class="s1">&#39;./examples/BayArea-Y3-Summary.csv&#39;</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="n">data_files_c</span> <span class="o">=</span>  <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span>
    <span class="n">data_files_w</span> <span class="o">=</span>  <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span>
    
    <span class="n">chicago</span> <span class="o">=</span> <span class="n">number_of_subscribers</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="c1">#print(chicago)</span>
    <span class="n">nyc</span> <span class="o">=</span> <span class="n">number_of_subscribers</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="c1">#print(nyc)</span>
    <span class="n">washington</span> <span class="o">=</span> <span class="n">number_of_subscribers</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    <span class="c1">#print(washington)</span>
    
    <span class="n">tot_trip_c</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="n">tot_trip_n</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="n">tot_trip_w</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    
    <span class="n">chicago_prop</span> <span class="o">=</span> <span class="n">chicago</span> <span class="o">/</span> <span class="n">tot_trip_c</span>
    <span class="n">nyc_prop</span> <span class="o">=</span> <span class="n">nyc</span> <span class="o">/</span> <span class="n">tot_trip_n</span>
    <span class="n">washington_prop</span> <span class="o">=</span> <span class="n">washington</span> <span class="o">/</span> <span class="n">tot_trip_w</span>
    
    <span class="k">if</span> <span class="n">chicago_prop</span> <span class="o">&gt;</span> <span class="n">nyc_prop</span> <span class="ow">and</span> <span class="n">chicago_prop</span> <span class="o">&gt;</span> <span class="n">washington_prop</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest propotion of subscribers recorded in chicago: </span><span class="si">{}</span><span class="s1"> &#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">chicago_prop</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>
    <span class="k">elif</span> <span class="n">nyc_prop</span> <span class="o">&gt;</span> <span class="n">washington_prop</span> <span class="ow">and</span> <span class="n">nyc_prop</span> <span class="o">&gt;</span> <span class="n">chicago_prop</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest propotion of subscribers recorded in nyc: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">nyc_prop</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="k">return</span> <span class="s1">&#39;The highest propotion of subscribers recorded in washington: </span><span class="si">{}</span><span class="s1"> &#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">washington_prop</span><span class="p">,</span><span class="mi">2</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="n">propotion</span><span class="p">(</span><span class="n">data_file</span><span class="p">))</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The highest propotion of subscribers recorded in nyc: 0.89
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<blockquote><p><strong>Tip</strong>: In order to add additional cells to a notebook, you can use the "Insert Cell Above" and "Insert Cell Below" options from the menu bar above. There is also an icon in the toolbar for adding new cells, with additional icons for moving the cells up and down the document. By default, new cells are of the code type; you can also specify the cell type (e.g. Code or Markdown) of selected cells from the Cell menu or the dropdown in the toolbar.</p>
</blockquote>
<p>Now, you will write your own code to continue investigating properties of the data.</p>
<p><strong>Question 4b</strong>: Bike-share systems are designed for riders to take short trips. Most of the time, users are allowed to take trips of 30 minutes or less with no additional charges, with overage charges made for trips of longer than that duration. What is the average trip length for each city? What proportion of rides made in each city are longer than 30 minutes?</p>
<p><strong>Answer</strong>:</p>
<ol>
<li>Average Trip for Each City:
 The Average trip length of Chicago: 17 minutes
 The Average trip length of nyc: 16 minutes
 The Average trip length of washington: 14 minutes</li>
<li>Proportion of rides made in each city are longer than 30 minutes:
 The propotion of Chicago: 0.08
 The propotion of nyc: 0.07
 The propotion of washington: 0.08</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[28]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## Use this and additional cells to answer Question 4b.                 ##</span>
<span class="c1">##                                                                      ##</span>
<span class="c1">## HINT: The csv module reads in all of the data as strings, including  ##</span>
<span class="c1">## numeric values. You will need a function to convert the strings      ##</span>
<span class="c1">## into an appropriate numeric type before you aggregate data.          ##</span>
<span class="c1">## TIP: For the Bay Area example, the average trip length is 14 minutes ##</span>
<span class="c1">## and 3.5% of trips are longer than 30 minutes.                        ##</span>

<span class="k">def</span> <span class="nf">trip_length</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">total_trip</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">number_of_trip</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">Avg</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">,</span> <span class="n">delimiter</span><span class="o">=</span><span class="s2">&quot;,&quot;</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="n">number_of_trip</span> <span class="o">+=</span> <span class="mi">1</span>
            <span class="c1">#print(row[&#39;duration&#39;])</span>
            <span class="n">total_trip</span> <span class="o">+=</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span>
        <span class="n">Avg</span> <span class="o">=</span> <span class="n">total_trip</span> <span class="o">/</span> <span class="n">number_of_trip</span>
        <span class="k">return</span> <span class="n">Avg</span>

<span class="k">def</span> <span class="nf">avg_length</span><span class="p">(</span><span class="n">avg</span><span class="p">):</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="n">data_files_c</span> <span class="o">=</span>  <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span>
    <span class="n">data_files_w</span> <span class="o">=</span>  <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span>
    <span class="n">data</span> <span class="o">=</span> <span class="s1">&#39;./examples/BayArea-Y3-Summary.csv&#39;</span>
    
    <span class="n">chicago</span> <span class="o">=</span> <span class="n">trip_length</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="n">nyc</span> <span class="o">=</span> <span class="n">trip_length</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="n">washington</span> <span class="o">=</span> <span class="n">trip_length</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    <span class="n">d</span> <span class="o">=</span> <span class="n">trip_length</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
    
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Average trip length of Chicago: </span><span class="si">{}</span><span class="s1"> minutes&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">chicago</span><span class="p">,</span><span class="mi">0</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Average trip length of nyc: </span><span class="si">{}</span><span class="s1"> minutes&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">nyc</span><span class="p">,</span><span class="mi">0</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Average trip length of washington: </span><span class="si">{}</span><span class="s1"> minutes&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">washington</span><span class="p">,</span><span class="mi">0</span><span class="p">)))</span>
    
    <span class="c1">#print(&#39;The Average trip length of bayarea: {} minutes&#39;.format(round(d,0)))</span>
    
    
<span class="n">avg_length</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The Average trip length of Chicago: 17.0 minutes
The Average trip length of nyc: 16.0 minutes
The Average trip length of washington: 19.0 minutes
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[29]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">prop_duration</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">count</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">filename</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">,</span> <span class="n">delimiter</span><span class="o">=</span><span class="s2">&quot;,&quot;</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span> <span class="o">&gt;</span> <span class="mi">30</span><span class="p">:</span>
                <span class="n">count</span> <span class="o">+=</span> <span class="mi">1</span>
        <span class="k">return</span> <span class="n">count</span>
        
<span class="k">def</span> <span class="nf">prop_length</span><span class="p">(</span><span class="n">propotion</span><span class="p">):</span>
    
    
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="n">data_files_c</span> <span class="o">=</span>  <span class="s1">&#39;./data/Chicago-2016-Summary.csv&#39;</span>
    <span class="n">data_files_w</span> <span class="o">=</span>  <span class="s1">&#39;./data/Washington-2016-Summary.csv&#39;</span>
    <span class="n">data</span> <span class="o">=</span> <span class="s1">&#39;./examples/BayArea-Y3-Summary.csv&#39;</span>
    
    <span class="n">total_trip_chicago</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="n">total_trip_nyc</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="n">total_trip_washington</span> <span class="o">=</span> <span class="n">trips_cities</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    
    
    <span class="n">dur_chicago</span> <span class="o">=</span> <span class="n">prop_duration</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">)</span>
    <span class="n">dur_nyc</span> <span class="o">=</span> <span class="n">prop_duration</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">)</span>
    <span class="n">dur_washington</span> <span class="o">=</span> <span class="n">prop_duration</span><span class="p">(</span><span class="n">data_files_w</span><span class="p">)</span>
    
    <span class="n">chicago</span> <span class="o">=</span> <span class="p">(</span><span class="n">dur_chicago</span> <span class="o">/</span> <span class="n">total_trip_chicago</span><span class="p">)</span> 
    <span class="n">nyc</span> <span class="o">=</span> <span class="p">(</span><span class="n">dur_nyc</span> <span class="o">/</span> <span class="n">total_trip_nyc</span><span class="p">)</span> 
    <span class="n">washington</span> <span class="o">=</span> <span class="p">(</span><span class="n">dur_washington</span> <span class="o">/</span> <span class="n">total_trip_washington</span><span class="p">)</span>
    
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The propotion of Chicago: </span><span class="si">{}</span><span class="s1"> &#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">chicago</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The propotion of nyc: </span><span class="si">{}</span><span class="s1"> &#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">nyc</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The propotion of washington: </span><span class="si">{}</span><span class="s1"> &#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">washington</span><span class="p">,</span><span class="mi">2</span><span class="p">)))</span>
    
<span class="n">prop_length</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The propotion of Chicago: 0.08 
The propotion of nyc: 0.07 
The propotion of washington: 0.11 
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><strong>Question 4c</strong>: Dig deeper into the question of trip duration based on ridership. Choose one city. Within that city, which type of user takes longer rides on average: Subscribers or Customers?</p>
<p><strong>Answer</strong>: Customers takes longer rides on average: 33.0 minutes</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[30]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## Use this and additional cells to answer Question 4c. If you have    ##</span>
<span class="c1">## not done so yet, consider revising some of your previous code to    ##</span>
<span class="c1">## make use of functions for reusability.                              ##</span>
<span class="c1">##                                                                     ##</span>
<span class="c1">## TIP: For the Bay Area example data, you should find the average     ##</span>
<span class="c1">## Subscriber trip duration to be 9.5 minutes and the average Customer ##</span>
<span class="c1">## trip duration to be 54.6 minutes. Do the other cities have this     ##</span>
<span class="c1">## level of difference?                                                ##</span>

<span class="k">def</span> <span class="nf">long_ride</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">total_trip_sub</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">total_trip_cus</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">number_of_subs</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">number_of_cus</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">avg_subs</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">avg_cus</span> <span class="o">=</span> <span class="mi">0</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">number_of_subs</span> <span class="o">+=</span> <span class="mi">1</span>
                <span class="n">total_trip_sub</span> <span class="o">+=</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span>
            <span class="k">elif</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Customer&#39;</span><span class="p">:</span>
                <span class="n">number_of_cus</span> <span class="o">+=</span> <span class="mi">1</span>
                <span class="n">total_trip_cus</span> <span class="o">+=</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span>
        <span class="n">avg_subs</span> <span class="o">=</span> <span class="n">total_trip_sub</span> <span class="o">/</span> <span class="n">number_of_subs</span>
        <span class="c1">#print(avg_subs)</span>
        <span class="n">avg_cus</span> <span class="o">=</span> <span class="n">total_trip_cus</span> <span class="o">/</span> <span class="n">number_of_cus</span>
        <span class="c1">#print(avg_cus)</span>
        
        <span class="k">if</span> <span class="n">avg_subs</span> <span class="o">&gt;</span> <span class="n">avg_cus</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Subscribers takes longer rides on average: </span><span class="si">{}</span><span class="s1"> minutes&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">avg_subs</span><span class="p">,</span><span class="mi">0</span><span class="p">)))</span>
        <span class="k">else</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Customers takes longer rides on average: </span><span class="si">{}</span><span class="s1"> minutes&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">avg_cus</span><span class="p">,</span><span class="mi">0</span><span class="p">)))</span>
            
                
    
    
    
    
<span class="n">long_ride</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Customers takes longer rides on average: 33.0 minutes
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='visualizations'></a></p>
<h3 id="Visualizations">Visualizations<a class="anchor-link" href="#Visualizations">&#182;</a></h3><p>The last set of values that you computed should have pulled up an interesting result. While the mean trip time for Subscribers is well under 30 minutes, the mean trip time for Customers is actually <em>above</em> 30 minutes! It will be interesting for us to look at how the trip times are distributed. In order to do this, a new library will be introduced here, <code>matplotlib</code>. Run the cell below to load the library and to generate an example plot.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[32]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># load library</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span><span class="p">;</span> <span class="n">plt</span><span class="o">.</span><span class="n">rcdefaults</span><span class="p">()</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">plotly.plotly</span> <span class="k">as</span> <span class="nn">py</span>

<span class="c1"># this is a &#39;magic word&#39; that allows for plots to be displayed</span>
<span class="c1"># inline with the notebook. If you want to know more, see:</span>
<span class="c1"># http://ipython.readthedocs.io/en/stable/interactive/magics.html</span>
<span class="o">%</span><span class="k">matplotlib</span> inline 

<span class="c1"># example histogram, data taken from bay area sample</span>
<span class="n">data</span> <span class="o">=</span> <span class="p">[</span> <span class="mf">7.65</span><span class="p">,</span>  <span class="mf">8.92</span><span class="p">,</span>  <span class="mf">7.42</span><span class="p">,</span>  <span class="mf">5.50</span><span class="p">,</span> <span class="mf">16.17</span><span class="p">,</span>  <span class="mf">4.20</span><span class="p">,</span>  <span class="mf">8.98</span><span class="p">,</span>  <span class="mf">9.62</span><span class="p">,</span> <span class="mf">11.48</span><span class="p">,</span> <span class="mf">14.33</span><span class="p">,</span>
        <span class="mf">19.02</span><span class="p">,</span> <span class="mf">21.53</span><span class="p">,</span>  <span class="mf">3.90</span><span class="p">,</span>  <span class="mf">7.97</span><span class="p">,</span>  <span class="mf">2.62</span><span class="p">,</span>  <span class="mf">2.67</span><span class="p">,</span>  <span class="mf">3.08</span><span class="p">,</span> <span class="mf">14.40</span><span class="p">,</span> <span class="mf">12.90</span><span class="p">,</span>  <span class="mf">7.83</span><span class="p">,</span>
        <span class="mf">25.12</span><span class="p">,</span>  <span class="mf">8.30</span><span class="p">,</span>  <span class="mf">4.93</span><span class="p">,</span> <span class="mf">12.43</span><span class="p">,</span> <span class="mf">10.60</span><span class="p">,</span>  <span class="mf">6.17</span><span class="p">,</span> <span class="mf">10.88</span><span class="p">,</span>  <span class="mf">4.78</span><span class="p">,</span> <span class="mf">15.15</span><span class="p">,</span>  <span class="mf">3.53</span><span class="p">,</span>
         <span class="mf">9.43</span><span class="p">,</span> <span class="mf">13.32</span><span class="p">,</span> <span class="mf">11.72</span><span class="p">,</span>  <span class="mf">9.85</span><span class="p">,</span>  <span class="mf">5.22</span><span class="p">,</span> <span class="mf">15.10</span><span class="p">,</span>  <span class="mf">3.95</span><span class="p">,</span>  <span class="mf">3.17</span><span class="p">,</span>  <span class="mf">8.78</span><span class="p">,</span>  <span class="mf">1.88</span><span class="p">,</span>
         <span class="mf">4.55</span><span class="p">,</span> <span class="mf">12.68</span><span class="p">,</span> <span class="mf">12.38</span><span class="p">,</span>  <span class="mf">9.78</span><span class="p">,</span>  <span class="mf">7.63</span><span class="p">,</span>  <span class="mf">6.45</span><span class="p">,</span> <span class="mf">17.38</span><span class="p">,</span> <span class="mf">11.90</span><span class="p">,</span> <span class="mf">11.52</span><span class="p">,</span>  <span class="mf">8.63</span><span class="p">,]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Distribution of Trip Durations&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration (m)&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In the above cell, we collected fifty trip times in a list, and passed this list as the first argument to the <code>.hist()</code> function. This function performs the computations and creates plotting objects for generating a histogram, but the plot is actually not rendered until the <code>.show()</code> function is executed. The <code>.title()</code> and <code>.xlabel()</code> functions provide some labeling for plot context.</p>
<p>You will now use these functions to create a histogram of the trip times for the city you selected in question 4c. Don't separate the Subscribers and Customers for now: just collect all of the trip times and plot them.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[33]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## Use this and additional cells to collect all of the trip times as a list ##</span>
<span class="c1">## and then use pyplot functions to generate a histogram of trip times.     ##</span>

<span class="k">def</span> <span class="nf">histogram_trip</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">new_trip</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="c1">#print(row[&#39;duration&#39;])</span>
            <span class="n">new_trip</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]),</span><span class="mi">2</span><span class="p">))</span>
        <span class="c1">#print(new_trip[:20])</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">new_trip</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Distribution of Trip Durations&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration (m)&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
            

<span class="n">histogram_trip</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>If you followed the use of the <code>.hist()</code> and <code>.show()</code> functions exactly like in the example, you're probably looking at a plot that's completely unexpected. The plot consists of one extremely tall bar on the left, maybe a very short second bar, and a whole lot of empty space in the center and right. Take a look at the duration values on the x-axis. This suggests that there are some highly infrequent outliers in the data. Instead of reprocessing the data, you will use additional parameters with the <code>.hist()</code> function to limit the range of data that is plotted. Documentation for the function can be found <a href="https://matplotlib.org/devdocs/api/_as_gen/matplotlib.pyplot.hist.html#matplotlib.pyplot.hist">[here]</a>.</p>
<p><strong>Question 5</strong>: Use the parameters of the <code>.hist()</code> function to plot the distribution of trip times for the Subscribers in your selected city. Do the same thing for only the Customers. Add limits to the plots so that only trips of duration less than 75 minutes are plotted. As a bonus, set the plots up so that bars are in five-minute wide intervals. For each group, where is the peak of each distribution? How would you describe the shape of each distribution?</p>
<p><strong>Answer</strong>:</p>
<ol>
<li><p>where is the peak of each distribution?
 a. Subscribers:</p>

<pre><code>     The Peak is at where X is:  6.5625

</code></pre>
<p>b. customers:</p>

<pre><code>     The Peak is at where X is:  21.7148         </code></pre>
</li>
<li><p>How would you describe the shape of each distribution?
  Both Customer and Subscriber distribution is possibly non-symmetric, the fact that it has only one peak makes it unimodal, and it's skewed right (postive skewness).</p>
</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[34]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## Use this and additional cells to answer Question 5. ##</span>

<span class="k">def</span> <span class="nf">histogram_subs</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">new_trip</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span> <span class="ow">and</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span> <span class="o">&lt;</span> <span class="mi">75</span><span class="p">:</span>
                <span class="n">new_trip</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]),</span><span class="mi">2</span><span class="p">))</span>
        <span class="c1">#print(new_trip)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">new_trip</span><span class="p">,</span><span class="n">bins</span><span class="o">=</span><span class="mi">5</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Distribution of Trip Durations&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration (m)&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
    
    <span class="c1">#Peak calculation</span>
    <span class="c1">#arr = np.array(list(new_trip))</span>
    <span class="n">y</span><span class="p">,</span><span class="n">x</span><span class="p">,</span><span class="n">_</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">new_trip</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="mi">200</span><span class="p">)</span>
    
    <span class="n">max_y</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>  <span class="c1"># Find the maximum y value</span>
    <span class="n">max_x</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">y</span><span class="p">)]</span>  <span class="c1"># Find the x value corresponding to the maximum y value</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Peak is at where X is: &#39;</span><span class="p">,</span><span class="n">max_x</span><span class="p">)</span>
 

            

<span class="n">histogram_subs</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The Peak is at where X is:  6.5625
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[35]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">histogram_cus</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">new_trip</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">data_files_n</span> <span class="o">=</span> <span class="s1">&#39;./data/NYC-2016-Summary.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_n</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>
            <span class="k">if</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;user_type&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="s1">&#39;Customer&#39;</span> <span class="ow">and</span> <span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">])</span> <span class="o">&lt;</span> <span class="mi">75</span><span class="p">:</span>
                <span class="n">new_trip</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="nb">float</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;duration&#39;</span><span class="p">]),</span><span class="mi">2</span><span class="p">))</span>
        <span class="c1">#print(new_trip)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">new_trip</span><span class="p">,</span><span class="n">bins</span><span class="o">=</span><span class="mi">5</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Distribution of Trip Durations&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Duration (m)&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
    
        <span class="c1">#Peak calculation</span>
    <span class="c1">#x,y,_=plt.hist(new_trip, bins=5)</span>
    
     <span class="c1">#Peak calculation</span>
    <span class="n">arr</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="n">new_trip</span><span class="p">))</span>
    <span class="n">y</span><span class="p">,</span><span class="n">x</span><span class="p">,</span><span class="n">_</span><span class="o">=</span><span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">arr</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="mi">200</span><span class="p">)</span>
    
    <span class="n">max_y</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>  <span class="c1"># Find the maximum y value</span>
    <span class="n">max_x</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">y</span><span class="p">)]</span>  <span class="c1"># Find the x value corresponding to the maximum y value</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Peak is at where X is: &#39;</span><span class="p">,</span><span class="n">max_x</span><span class="p">)</span>
    
    
    <span class="c1">#print(&#39;The Peak at X where Y is at : &#39;,x.max())</span>
    
            

<span class="n">histogram_cus</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>The Peak is at where X is:  21.7148
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='eda_continued'></a></p>
<h2 id="Performing-Your-Own-Analysis">Performing Your Own Analysis<a class="anchor-link" href="#Performing-Your-Own-Analysis">&#182;</a></h2><p>So far, you've performed an initial exploration into the data available. You have compared the relative volume of trips made between three U.S. cities and the ratio of trips made by Subscribers and Customers. For one of these cities, you have investigated differences between Subscribers and Customers in terms of how long a typical trip lasts. Now it is your turn to continue the exploration in a direction that you choose. Here are a few suggestions for questions to explore:</p>
<ul>
<li>How does ridership differ by month or season? Which month / season has the highest ridership? Does the ratio of Subscriber trips to Customer trips change depending on the month or season?</li>
<li>Is the pattern of ridership different on the weekends versus weekdays? On what days are Subscribers most likely to use the system? What about Customers? Does the average duration of rides change depending on the day of the week?</li>
<li>During what time of day is the system used the most? Is there a difference in usage patterns for Subscribers and Customers?</li>
</ul>
<p>If any of the questions you posed in your answer to question 1 align with the bullet points above, this is a good opportunity to investigate one of them. As part of your investigation, you will need to create a visualization. If you want to create something other than a histogram, then you might want to consult the <a href="https://matplotlib.org/devdocs/api/pyplot_summary.html">Pyplot documentation</a>. In particular, if you are plotting values across a categorical variable (e.g. city, user type), a bar chart will be useful. The <a href="https://matplotlib.org/devdocs/api/_as_gen/matplotlib.pyplot.bar.html#matplotlib.pyplot.bar">documentation page for <code>.bar()</code></a> includes links at the bottom of the page with examples for you to build off of for your own use.</p>
<p><strong>Question 6</strong>: Continue the investigation by exploring another question that could be answered by the data available. Document the question you want to explore below. Your investigation should involve at least two variables and should compare at least two groups. You should also use at least one visualization as part of your explorations.</p>
<p><strong>Answer</strong>:</p>
<ol>
<li>Trip Duration Month wise (Trips vs Months)</li>
<li>Trip Duration Season wise (Trips vs Seasons)</li>
<li>Highest Trip Duration of the Month in a year</li>
<li>Highest Trip Duration of the Season in a year</li>
<li>Trip Duration Ratio b/w subscribers to customers - Month wise</li>
<li>Trip Duration Ratio b/w subscribers to customers - Season wise</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">## Use this and additional cells to continue to explore the dataset. ##</span>
<span class="c1">## Once you have performed your exploration, document your findings  ##</span>
<span class="c1">## in the Markdown cell above.                                       ##</span>
<span class="k">def</span> <span class="nf">ride_month</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">month_list</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">month_dict</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="n">data_files_c</span> <span class="o">=</span> <span class="s1">&#39;./data/Chicago-Divvy-2016.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span>       
            <span class="n">t</span> <span class="o">=</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">]</span>
            <span class="n">mymonth</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">t</span><span class="p">,</span><span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
            <span class="n">month</span> <span class="o">=</span> <span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%b&#39;</span><span class="p">)</span>
            <span class="n">month_list</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">month</span><span class="p">)</span>
        
        <span class="n">my_dict</span> <span class="o">=</span> <span class="p">{</span><span class="n">i</span><span class="p">:</span><span class="n">month_list</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="n">i</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">month_list</span><span class="p">}</span>
        <span class="c1">#print(my_dict)</span>
    <span class="k">return</span> <span class="n">my_dict</span>
            
<span class="k">def</span> <span class="nf">month_list</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">my_months</span> <span class="o">=</span> <span class="n">ride_month</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    <span class="c1">#print(my_months)</span>
    <span class="n">months</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jan&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Feb&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Mar&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Apr&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;May&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jun&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jul&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Aug&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Sep&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Oct&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Nov&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">)</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Dec&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">)</span>
    
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Jan: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Feb: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Mar: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Apr: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of May: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Jun: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Jul: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Aug: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Sep: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Oct: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Nov: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Dec: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">((</span><span class="n">my_months</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="s1">&#39;No rides recorded&#39;</span><span class="p">))))</span>
    
    
    <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">months</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">months</span><span class="o">.</span><span class="n">values</span><span class="p">()),</span> <span class="n">align</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">months</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">months</span><span class="o">.</span><span class="n">keys</span><span class="p">()))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Trips&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Number of Rides vs Month&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>

    


<span class="k">def</span> <span class="nf">season_list</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">my_season</span> <span class="o">=</span> <span class="n">ride_month</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    
    <span class="n">season</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jan-Mar&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Apr-Jun&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jul-Sep&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Oct-Dec&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">my_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    
    
    
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Jan-Mar: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jan-Mar&#39;</span><span class="p">]))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Apr-Jun: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Apr-Jun&#39;</span><span class="p">]))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Jul-Sep: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jul-Sep&#39;</span><span class="p">]))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;No.of rides in the Month of Oct-Dec: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Oct-Dec&#39;</span><span class="p">]))</span>
    
    <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">season</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">season</span><span class="o">.</span><span class="n">values</span><span class="p">()),</span> <span class="n">align</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">season</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">season</span><span class="o">.</span><span class="n">keys</span><span class="p">()))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Trips&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Number of Rides vs Season&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
            
<span class="n">month_list</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span> 
<span class="n">season_list</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>No.of rides in the Month of Jan: 1901
No.of rides in the Month of Feb: 2394
No.of rides in the Month of Mar: 3719
No.of rides in the Month of Apr: 4567
No.of rides in the Month of May: 7211
No.of rides in the Month of Jun: 9794
No.of rides in the Month of Jul: 10286
No.of rides in the Month of Aug: 9810
No.of rides in the Month of Sep: 8700
No.of rides in the Month of Oct: 7160
No.of rides in the Month of Nov: 4811
No.of rides in the Month of Dec: 1778
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>No.of rides in the Month of Jan-Mar: 8014
No.of rides in the Month of Apr-Jun: 21572
No.of rides in the Month of Jul-Sep: 28796
No.of rides in the Month of Oct-Dec: 13749
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">high_month</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">high_month</span> <span class="o">=</span> <span class="n">ride_month</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    <span class="n">max_m</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="n">high_month</span><span class="o">.</span><span class="n">items</span><span class="p">(),</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Highest month recorded with trips: &#39;</span><span class="p">,</span><span class="n">max_m</span><span class="p">)</span>
    
<span class="k">def</span> <span class="nf">high_season</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">high_season</span> <span class="o">=</span> <span class="n">ride_month</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    <span class="n">season1</span> <span class="o">=</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">season2</span> <span class="o">=</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">season3</span> <span class="o">=</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    <span class="n">season4</span> <span class="o">=</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">+</span> <span class="n">high_season</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span>
    
    <span class="k">if</span> <span class="nb">int</span><span class="p">(</span><span class="n">season1</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season2</span><span class="p">)</span> <span class="ow">and</span> <span class="nb">int</span><span class="p">(</span><span class="n">season1</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season3</span><span class="p">)</span> <span class="ow">and</span> <span class="nb">int</span><span class="p">(</span><span class="n">season1</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season4</span><span class="p">):</span>
        <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Highest recorded season is between Jan-Mar with trips: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season1</span><span class="p">))</span>
    <span class="k">elif</span> <span class="nb">int</span><span class="p">(</span><span class="n">season2</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season1</span><span class="p">)</span> <span class="ow">and</span> <span class="nb">int</span><span class="p">(</span><span class="n">season2</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season3</span><span class="p">)</span> <span class="ow">and</span> <span class="nb">int</span><span class="p">(</span><span class="n">season2</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season4</span><span class="p">):</span>
        <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Highest recorded season is between Apr-Jun with trips: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season2</span><span class="p">))</span>
    <span class="k">elif</span> <span class="nb">int</span><span class="p">(</span><span class="n">season3</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season1</span><span class="p">)</span> <span class="ow">and</span> <span class="nb">int</span><span class="p">(</span><span class="n">season3</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season2</span><span class="p">)</span> <span class="ow">and</span> <span class="nb">int</span><span class="p">(</span><span class="n">season3</span><span class="p">)</span> <span class="o">&gt;</span> <span class="nb">int</span><span class="p">(</span><span class="n">season4</span><span class="p">):</span>
        <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Highest recorded season is between Jul-Sep with trips: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season3</span><span class="p">))</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;The Highest recorded season is between Oct-Dec with trips: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">season4</span><span class="p">))</span>
            
<span class="n">high_season</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
<span class="n">high_month</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">ratio_subs</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">month_list</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">month_dict</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="n">data_files_c</span> <span class="o">=</span> <span class="s1">&#39;./data/Chicago-Divvy-2016.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span> 
            <span class="k">if</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;usertype&#39;</span><span class="p">])</span> <span class="o">==</span> <span class="s1">&#39;Subscriber&#39;</span><span class="p">:</span>
                <span class="n">t</span> <span class="o">=</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">]</span>
                <span class="n">mymonth</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">t</span><span class="p">,</span><span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
                <span class="n">month</span> <span class="o">=</span> <span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%b&#39;</span><span class="p">)</span>
                <span class="n">month_list</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">month</span><span class="p">)</span>
        
        <span class="n">my_dict</span> <span class="o">=</span> <span class="p">{</span><span class="n">i</span><span class="p">:</span><span class="n">month_list</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="n">i</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">month_list</span><span class="p">}</span>
        <span class="c1">#print(my_dict)</span>
    <span class="k">return</span> <span class="n">my_dict</span>

<span class="k">def</span> <span class="nf">ratio_cus</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">month_list</span> <span class="o">=</span> <span class="p">[]</span>
    <span class="n">month_dict</span> <span class="o">=</span> <span class="p">{}</span>
    <span class="n">data_files_c</span> <span class="o">=</span> <span class="s1">&#39;./data/Chicago-Divvy-2016.csv&#39;</span>
    <span class="k">with</span> <span class="nb">open</span><span class="p">(</span><span class="n">data_files_c</span><span class="p">,</span><span class="s1">&#39;r&#39;</span><span class="p">)</span> <span class="k">as</span> <span class="n">f</span><span class="p">:</span>
        <span class="n">trip_reader</span> <span class="o">=</span> <span class="n">csv</span><span class="o">.</span><span class="n">DictReader</span><span class="p">(</span><span class="n">f</span><span class="p">)</span>
        
        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">trip_reader</span><span class="p">:</span> 
            <span class="k">if</span><span class="p">(</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;usertype&#39;</span><span class="p">])</span> <span class="o">==</span> <span class="s1">&#39;Customer&#39;</span><span class="p">:</span>
                <span class="n">t</span> <span class="o">=</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;starttime&#39;</span><span class="p">]</span>
                <span class="n">mymonth</span> <span class="o">=</span> <span class="n">datetime</span><span class="o">.</span><span class="n">strptime</span><span class="p">(</span><span class="n">t</span><span class="p">,</span><span class="s1">&#39;%m/</span><span class="si">%d</span><span class="s1">/%Y %H:%M&#39;</span><span class="p">)</span>
                <span class="n">month</span> <span class="o">=</span> <span class="n">mymonth</span><span class="o">.</span><span class="n">strftime</span><span class="p">(</span><span class="s1">&#39;%b&#39;</span><span class="p">)</span>
                <span class="n">month_list</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">month</span><span class="p">)</span>
        
        <span class="n">my_dict</span> <span class="o">=</span> <span class="p">{</span><span class="n">i</span><span class="p">:</span><span class="n">month_list</span><span class="o">.</span><span class="n">count</span><span class="p">(</span><span class="n">i</span><span class="p">)</span> <span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">month_list</span><span class="p">}</span>
        <span class="c1">#print(my_dict)</span>
    <span class="k">return</span> <span class="n">my_dict</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">month_ratio</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">month_subs</span> <span class="o">=</span> <span class="n">ratio_subs</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    <span class="n">month_cus</span> <span class="o">=</span> <span class="n">ratio_cus</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    
    <span class="n">months</span> <span class="o">=</span> <span class="p">{}</span>
    
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jan&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Feb&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Mar&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Apr&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;May&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jun&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jul&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Aug&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Sep&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Oct&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Nov&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">months</span><span class="p">[</span><span class="s1">&#39;Dec&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="nb">float</span><span class="p">(</span><span class="n">month_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">month_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    
    
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Jan: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jan&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Feb: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Feb&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Mar: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Mar&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Apr: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Apr&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of May: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;May&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Jun: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jun&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Jul: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Jul&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Aug: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Aug&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Sep: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Sep&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Oct: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Oct&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Nov: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Nov&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the Month of Dec: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">months</span><span class="p">[</span><span class="s1">&#39;Dec&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>

    
    <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">months</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">months</span><span class="o">.</span><span class="n">values</span><span class="p">()),</span> <span class="n">align</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">months</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">months</span><span class="o">.</span><span class="n">keys</span><span class="p">()))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Trips&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Ratio of Subscribers to Customers vs Month&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
    
<span class="n">month_ratio</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[55]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">season_ratio</span><span class="p">(</span><span class="n">filename</span><span class="p">):</span>
    <span class="n">season_subs</span> <span class="o">=</span> <span class="n">ratio_subs</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    <span class="n">season_cus</span> <span class="o">=</span> <span class="n">ratio_cus</span><span class="p">(</span><span class="n">filename</span><span class="p">)</span>
    
    <span class="n">season</span><span class="o">=</span> <span class="p">{}</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jan-Mar&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jan&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Feb&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Mar&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Apr-Jun&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Apr&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;May&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jun&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jul-Sep&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Jul&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Aug&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Sep&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    <span class="n">season</span><span class="p">[</span><span class="s1">&#39;Oct-Dec&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Oct&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Nov&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span> <span class="o">+</span> <span class="p">(</span><span class="n">season_subs</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="o">/</span> <span class="n">season_cus</span><span class="o">.</span><span class="n">get</span><span class="p">(</span><span class="s1">&#39;Dec&#39;</span><span class="p">,</span><span class="mi">0</span><span class="p">))</span>
    
    
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the season of Jan-Mar: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jan-Mar&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the season of Apr-Jun: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Apr-Jun&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the season of Jul-Sep: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Jul-Sep&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Ratio of subscribers to customers in the season of Oct-Dec: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="nb">round</span><span class="p">(</span><span class="n">season</span><span class="p">[</span><span class="s1">&#39;Oct-Dec&#39;</span><span class="p">],</span><span class="mi">2</span><span class="p">)))</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">season</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">season</span><span class="o">.</span><span class="n">values</span><span class="p">()),</span> <span class="n">align</span><span class="o">=</span><span class="s1">&#39;center&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">season</span><span class="p">)),</span> <span class="nb">list</span><span class="p">(</span><span class="n">season</span><span class="o">.</span><span class="n">keys</span><span class="p">()))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Trips&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Ratio of Subscribers to Customers vs Season&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
    
<span class="n">season_ratio</span><span class="p">(</span><span class="n">data_file</span><span class="p">)</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Ratio of subscribers to customers in the season of Jan-Mar: 44.74
Ratio of subscribers to customers in the season of Apr-Jun: 8.82
Ratio of subscribers to customers in the season of Jul-Sep: 7.35
Ratio of subscribers to customers in the season of Oct-Dec: 38.65
</pre>
</div>
</div>

<div class="output_area">

<div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYIAAAEICAYAAABS0fM3AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMS4wLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvpW3flQAAGopJREFUeJzt3Xm4XHWd5/H3JwlLIOxcGEIiQYjIIgYIW+MSWVq21kBDS0RMFKSZHgfoRgWZ1gEERB8RmMYeBEHjiGHVBkFH6EhkUAgk7GExbEIESVgCBAEJfOeP3+/CSVFV9yY3pyqX3+f1PPXcOvv3LHU+Z6u6igjMzKxcQ7pdgJmZdZeDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA6CLpF0qKTrahjvcEm/kPSCpMuX87inSLppeY6zxXTmSJqQ358k6Sd1T9OsZA6CfpL0mKRXJC2S9GdJP5I0op/DjpEUkob1touIiyPib2so9SBgQ2C9iDi4SS1rS7ooz8NLkv4g6fga6lhmEbF1RMzoZg2SJkiaN8BxbCTpQklP5WX9gKSTJa0+wPGGpM0HMo7BTNKJkh7Nn8V5ki7tdk2DnYNg6fxdRIwAxgHbAV/tcj3NbAL8ISIWt+h+FjAC2BJYC/gE8HCHamurGpSDcfwN01oXuBkYDuwaEWsAewFrA5t1qo46dXJ5VqY5GTgM2DN/FscD0ztdx7tORPjVjxfwGGnj623+NnBtpXk/4A7gReAJ4KRKt8eBABbl167AFOCmSj9/A9wGvJD//k2bWrYEZgALgTnAJ3L7k4G/Aq/n6RzeZNh7gYktxjsm1zms0m4GcER+PwX4HfBvuc4HgD0q/U4BHgFeAh4FDq10+wJwf+52H7B9ZbkeD9wNvAYMqy5r4CTgCuDSPOztwAcr4x0JXAksyNM8utKtd9if5PVyBLATMCs3Pw18t8lyWB14BXizss5GAqsAZwNP5tfZwCotluWpwD3AkGVc1psDv83L+Rng0tz+xjzcy7muT1WW70PAc8DVwMjKeAP4J2BuXobfIIXRzXk5XAasXOl/f+BO0vb1e2Dbhs9B4/o6HvhTHveD1W2iMtwuwJ+BoZV2BwB35/d9rpfc37nA2W0+G2sBFwJP5ZpO7Z1mnuffAM/mZXoxsHZl2Kbz0W69AxOAecBxwPw83c91e3+1tK+uFzBYXiy5cxqVP+TnVLpPAD5AOsvaNm/ME3O3Zh/6KeQgANYFnicd6QwDJuXm9ZrUsVL+wJ8IrAzsnjfcLXL3k4CftJmPH5DC43PA2IZuzeqcwZJBsBj451zHp0g7qnVJO88XK3VsBGyd3x+cP2A7AiLt5DapLNc7gdHA8CbL+iRSsB2Up/kl0g5/pbysZwNfz8vivaQg+njDsBNzv8NJO7/DcvcRwC4tltMEYF5Du1OAW4ANgB7STvIbLYa/BTi5zXroa1lPA/5HrntV4EOV/gLYvNK8O2nHtj1pp/VvwI0N/V8NrAlsTdqBT8/Lay1SME/O/W5P2qHtDAwFJuf10bvjW2J9AVuQDnxGVuZrsxbz/DCwV6X5cuCE/L6/6+UzpLD7MulsYGhD9/8Avk/aHjcAbgX+MXfbnHRWtkpefzeSQ6XdfLRb73k7WZz7WQnYF/gLsE6391lL8+p6AYPllT8Ai0g73cgfpLXb9H82cFZlo2oXBIcBtzYMfzMwpcl4P0w6shpSaTeNfAZC30EwnBQis0k7yYeAfdrUOYMlg+BJQJXut+b6VycdQf49eYde6efXwDFtluvnm7SrBsEtlW5DSEddHybtrB5vGParwA8rw97Y0P1G0pnT+n2s7wm8MwgeBvatNH8ceKzF8HOBo9qMv69l/WPgfGBUk2Ebg+BC4NuV5hF53Y6p9L9bpfts4PhK85m8vUP83zSEG+no+KPN1hdp5zof2BNYqY9leipwUX6/BumsZpOlWS+530OB/8zDP8vbYbIhKeSGV/qdBNzQYjwTgTv6mo926z1vJ680rMf5tAiyFfXlewRLZ2Kka70TgPcD6/d2kLSzpBskLZD0AnBUtXsfRgJ/bGj3R2DjFv0+ERFv9qPfd4iIVyLi9IjYAViPdFng8nxNuz/+FHlrr0x7ZES8TDpDOAp4StK1kt6f+xlN+/sQT/Qxzbe65/meR1oOmwAjJS3sfZFCbsM24z4ceB/wgKTbJO3fx7SrGtfTH3O7Zp4lnRUtq6+Qzp5uzU9Rfb6/dUXEojz96jbxdOX9K02aex982AQ4rmGZjmbJ+ayuj4eAY0mhO1/SJZJaLZOfAgdKWgU4ELg9Inrr7vd6ifSgxZ6k+y1HAadI+niufSXS9tdb+/dJR/JI2iDX9ydJL5IuGa7fj/noa70/G0vek/sLby/PQcFBsAwi4rfAj4DvVFr/lHT6PToi1gLOI32QIR2RtfMkaSOueg/pckqzfkdLGtKPftuKiBeB00lH85uSjrAAVqv09l8aBttYkirN78k1ERG/joi9SDvAB4ALcj9P0P4GaV/LZ3Tvmzzfo/I0nwAejYi1K681ImLfVuOOiLkRMYm0c/gWcEWLp3ia1dS4nt6a9yb+EzigYT1VtV3WEfHniPhCRIwE/hH49zZPCi1RV56f9ViGbYK0TE9rWKarRcS0Sj+Ny/SnEfGhXEOQlus7RMR9pJ3oPsCnSZ+Z3m79XS/V8b0eEZeT7ldsk2t/jXRW0Vv7mhGxdR7km7m+bSNiTdJlJlXG12o+lma9D0oOgmV3NrCXpHG5eQ3guYh4VdJOpA291wLSjcf3thjXL4H3Sfq0pGGSPgVsBVzTpN+ZpJ3IVyStlJ+3/zvgkv4ULelrknaUtLKkVYFjSJd0HoyIBaSdx2ckDc1HoY078A2Ao/O0DybduP6lpA0lfSJ/eF8jXUZ7Iw/zA+BLknZQsrmkxuBrZwdJB+anVI7N47+FdFnqRUnH5+9PDJW0jaQd28z/ZyT15DOLhbn1G016fRpYT9JalXbTgH+V1CNpfdK9iVbfcfgu6Zr81N55lbSxpO9K2ravZS3pYEmjcuPzpB1Tb51Ps+S29FPgc5LG5aPt04GZEfFYq+XQxgXAUfkMV5JWl7SfpDWa9SxpC0m75+m+Sjq7aLY8q7UeDXyEdI+gdzz9Wi9K32XZT9IakoZI2od032NmRDwFXAecKWnN3H0zSR/Ng69B2i4XStqYdJ+hP/OxNOt9UHIQLKP8Qf4x8LXc6p9Ip6gvkTaUyyr9/gU4DfhdPmXdpWFcz5Ke1DiOdEr/FWD/iHimyXT/Snrkcx/SDcJ/Bz4bEQ/0t3Tgh3nYJ0k3z/bLlxMgPX3y5VzH1qQbY1UzgbF5+NOAg3L9Q3L9T5Ju5n00LxPyUdtppJ3AS6Qbev29FAVwFemyU+8N9QPz0eAbpBAcR7qB/AwpdNZqNSJgb2COpEXAOcAhEfFqY095eU4DHsnrbCTpGvcs0hHoPaQnmE5tNpGIeI70JNjrwMy8XUwn3Vx/KPfWblnvmIdbRDrTPCYiHs3dTiIFzEJJ/xAR00nb4ZWk+yebAYe0WQYtRcSsXNe5pOX9EOneUCurAGeQlv2fSQcKJ7bpfxrp0upvGrbvfq0X0gMJJ5KexFtIenrvv0ZE7xcdP0t6cOC+XP8VvH2J7mTSzfAXgGuBn/VzPvq93gcrLXm518zMSuMzAjOzwjkIzMwK5yAwMyucg8DMrHAd/9GoZbH++uvHmDFjul2GmdmgMnv27Gcioqev/gZFEIwZM4ZZs2Z1uwwzs0FFUuMvFjTlS0NmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoUbFN8sHogxJ1zb7RK66rEz9ut2CWa2gvMZgZlZ4RwEZmaFcxCYmRXOQWBmVjgHgZlZ4RwEZmaFcxCYmRXOQWBmVjgHgZlZ4RwEZmaFcxCYmRXOQWBmVjgHgZlZ4RwEZmaFcxCYmRXOQWBmVjgHgZlZ4RwEZmaFqz0IJA2VdIeka3LzppJmSpor6VJJK9ddg5mZtdaJM4JjgPsrzd8CzoqIscDzwOEdqMHMzFqoNQgkjQL2A36QmwXsDlyRe5kKTKyzBjMza6/uM4Kzga8Ab+bm9YCFEbE4N88DNm42oKQjJc2SNGvBggU1l2lmVq7agkDS/sD8iJhdbd2k12g2fEScHxHjI2J8T09PLTWamRkMq3HcuwGfkLQvsCqwJukMYW1Jw/JZwSjgyRprMDOzPtR2RhARX42IURExBjgE+E1EHArcAByUe5sMXFVXDWZm1rdufI/geOBfJD1EumdwYRdqMDOzrM5LQ2+JiBnAjPz+EWCnTkzXzMz61pEgMDNbFmNOuLbbJXTVY2fs15Hp+CcmzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwjkIzMwK5yAwMyucg8DMrHAOAjOzwtUWBJJWlXSrpLskzZF0cm6/qaSZkuZKulTSynXVYGZmfavzjOA1YPeI+CAwDthb0i7At4CzImIs8DxweI01mJlZH2oLgkgW5caV8iuA3YErcvupwMS6ajAzs77Veo9A0lBJdwLzgeuBh4GFEbE49zIP2LjFsEdKmiVp1oIFC+os08ysaLUGQUS8ERHjgFHATsCWzXprMez5ETE+Isb39PTUWaaZWdE68tRQRCwEZgC7AGtLGpY7jQKe7EQNZmbWXJ1PDfVIWju/Hw7sCdwP3AAclHubDFxVVw1mZta3YX33ssw2AqZKGkoKnMsi4hpJ9wGXSDoVuAO4sMYazMysD7UFQUTcDWzXpP0jpPsFZma2AvA3i83MCucgMDMrnIPAzKxwDgIzs8I5CMzMCucgMDMrnIPAzKxwDgIzs8I5CMzMCucgMDMrnIPAzKxwDgIzs8I5CMzMCucgMDMrXJ9BIOmbktaUNEzSryU9LenTnSjOzMzq158zgn0i4kVgf9I/od8aOL7WqszMrGP6EwS9/7xmX2BaRDxDi384b2Zmg09//kPZryTdC7wB/DdJ6wOv1VuWmZl1Sp9nBBHxZWB3YIeIeB14BTiw7sLMzKwz+jwjkLQKcAjwIUkB3AScX3dhZmbWGf25NDSVdCnogtw8Kbc7pK6izMysc/oTBFtFxLaV5usl3VVXQWZm1ln9eWroTkk79jZI2gG4ub6SzMysk/pzRrA9cIukR3PzpsAcSXcAERHb11admZnVrj9B8MnaqzAzs65pGQSSVo+Il4EFzbrnbxubmdkg1+6M4ApgH2AO6ZvEavj7ntqrMzOz2rUMgojYR5KAnSPiyQ7WZGZmHdT2qaGICOAXHarFzMy6oD+Pj94qyU8GmZm9S7W7WTwsIhYDHwK+IOlh4GXyPQI/Nmpm9u7Q7mbxraTvEEzsUC1mZtYF7YJAABHxcIdqMTOzLmgXBD2S/qVVx4j4bg31mJlZh7ULgqHACPKZgZmZvTu1C4KnIuKUjlViZmZd0e7xUZ8JmJkVoF0Q7DGQEUsaLekGSfdLmiPpmNx+XUnXS5qb/64zkOmYmdnAtAyCiHhugONeDBwXEVsCu5D+8f1WwAnA9IgYC0zPzWZm1iX9+WbxMomIpyLi9vz+JeB+YGPSz1pPzb1Nxd9TMDPrqtqCoErSGGA7YCawYUQ8BSksgA1aDHOkpFmSZi1Y0PSXsM3MbDmoPQgkjQCuBI5dmv9hEBHnR8T4iBjf09NTX4FmZoWrNQgkrUQKgYsj4me59dOSNsrdNwLm11mDmZm1V1sQ5P9lcCFwf8O3kK8GJuf3k4Gr6qrBzMz61p//WbysdgMOA+6RdGdudyJwBnCZpMOBx4GDa6zBzMz6UFsQRMRNtP5S2oC+o2BmZstPR54aMjOzFZeDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK5yDwMyscA4CM7PCOQjMzArnIDAzK1xtQSDpIknzJd1babeupOslzc1/16lr+mZm1j91nhH8CNi7od0JwPSIGAtMz81mZtZFtQVBRNwIPNfQ+pPA1Px+KjCxrumbmVn/dPoewYYR8RRA/rtBh6dvZmYNVtibxZKOlDRL0qwFCxZ0uxwzs3etTgfB05I2Ash/57fqMSLOj4jxETG+p6enYwWamZWm00FwNTA5v58MXNXh6ZuZWYM6Hx+dBtwMbCFpnqTDgTOAvSTNBfbKzWZm1kXD6hpxRExq0WmPuqZpZmZLr7YgsHeHMSdc2+0SuuqxM/brdglmtVthnxoyM7POcBCYmRXOQWBmVjgHgZlZ4RwEZmaFcxCYmRXOj4+a1ciP3/rx28HAZwRmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFc5BYGZWOAeBmVnhHARmZoVzEJiZFa4rQSBpb0kPSnpI0gndqMHMzJKOB4GkocD3gH2ArYBJkrbqdB1mZpZ044xgJ+ChiHgkIv4KXAJ8sgt1mJkZoIjo7ASlg4C9I+KI3HwYsHNEfLGhvyOBI3PjFsCDHS10+VkfeKbbRQxiXn4D4+U3MIN9+W0SET199TSsE5U0UJN270ijiDgfOL/+cuolaVZEjO92HYOVl9/AePkNTCnLrxuXhuYBoyvNo4Anu1CHmZnRnSC4DRgraVNJKwOHAFd3oQ4zM6MLl4YiYrGkLwK/BoYCF0XEnE7X0UGD/vJWl3n5DYyX38AUsfw6frPYzMxWLP5msZlZ4RwEZmaFcxC0IWnRchpPSPo/leZhkhZIumZ5jH9FJumAPP/vH+B4xki6d3nVNZj0tR1KmiHpHY84SlpN0sWS7pF0r6SbJI2or9IVh6RRkq6SNFfSw5LOyQ+ntOr/WEmrteg2QdILku7IP41zo6T966u+8xwEnfEysI2k4bl5L+BPSzMCSd34zsfyMAm4ifR0WL/lnyKxgTkGeDoiPhAR2wCHA693uabaSRLwM+A/ImIs8D5gBHBam8GOBZoGQfb/ImK7iNgCOBo4V9Iey6vmbnMQ9EHSCEnTJd2ej6w+mduPkXS/pAskzZF0XWVH38yvgP3y+0nAtMo0dpL0+3zE8XtJW+T2UyRdLukXwHU1zWJt8tHnbqQd0CG53YR8RPVzSfdJOk/SkNxtkaRTJM0Edm0z3imSzq00XyNpQmUcp0m6S9ItkjascRY7Ji+3ayrN50qa0sdgG1E54IiIByPitTz8ZyTdKulOSd/vDd68/M7M2/t0SX1+K3UFtDvwakT8ECAi3gD+Gfi8pNUlfSd/lu+W9N8lHQ2MBG6QdENfI4+IO4FTgC8CSOqRdKWk2/Jrt9x+hKQfVqb19zXN74A5CPr2KnBARGwPfAw4Mx9xAIwFvhcRWwMLgXYr+hLgEEmrAtsCMyvdHgA+EhHbAV8HTq902xWYHBG7L5e56ayJwP+NiD8Az0naPrffCTgO+ACwGXBgbr86cG9E7BwRNy3jNFcHbomIDwI3Al9Y5uoHv4uA4yXdLOlUSWMBJG0JfArYLSLGAW8Ah+ZhVgduz9v7b4H/2YW6B2prYHa1RUS8CDwOHAFsCmwXEdsCF0fE/yJ9qfVjEfGxfk7jdqD3cuc5wFkRsSNpH/CD3P5rwAv5jGxb4DcDmKdaDdbLDZ0k4HRJHwHeBDYGeo8yH81HB5A2vDGtRhIRd0saQzob+GVD57WAqfmDGsBKlW7XR8RzA5yHbpkEnJ3fX5KbrwVujYhHACRNAz4EXEHaIV05wGn+Feg9cp5NugxXpIi4U9J7gb8F9gRuk7QrsAewQ24GGA7Mz4O9CVya3/+EdIllsBFNfrYmt/8IcF5ELAYYwGer+lM5ewJbvX18yJqS1sjt37okGhHPL+O0aucg6NuhQA+wQ0S8LukxYNXc7bVKf28AwyWNBn6R250XEedV+rka+A4wAViv0v4bwA0RcUAOixmVbi8vl7noMEnrkU7Rt5EUpC8PBikEGz+kvc2v5tN4JO0MfD+3/zpwd6X/xSx5Nrtq5f3r8faXY97g3bONt5tnIN2Y5+0j+CMiYlZELCLtzH8m6U1gX1JYTo2Ir/ZjuoPxi0ZzaDg7l7Qm6adtHqGPeWpcji162w64P78fAuwaEa80jKdVIK1wfGmob2sB83MIfAzYpF3PEfFERIzLr/MaOl8EnBIR9zSZRu+13CnLo+gVwEHAjyNik4gYExGjgUdJR/87Kf3EyBDSJYp3XAaKiJmV5dj4EySPAeMkDcnBu1O9s7JC+CPpqHMVSWuRjuqXEBE/ryyzWZJ2k7QOQH5iZqs8nunAQZI2yN3WldS7XQ8hrTuAT9Nk3QwC04HVJH0W3nrw4EzgR6R7bUf1Pnwhad08zEvAGvDO5dg4cknbki77fC+3uo58vyB3H9ei/TrLawaXNwdBC3lDeQ24GBgvaRbp7OCBZR1nRMyLiHOadPo28E1JvyMdOb8bTAJ+3tDuStLO5WbgDOBeUjg09tdM7/oA+F0e7h7SGdbty6HeFVLvdhgRTwCXkc6MLgbu6MfgmwG/lXRP7n8WcGVE3Af8K3CdpLuB60k3liGdgW4taTbpjO6U5Tk/nZDPCA8ADpY0F/gD6V7fiaTr948Dd0u6i7Q9QvopiV+1uVn84fwwx4OkADg6IqbnbkeT9hF3S7oPOCq3PxVYR+nR3btI9xhXSP6JiRYkfRC4ICJKONrsmPx0z5ciYqmew1Z6WuvQiPiHWgpbQXV6O5S0KCKK+K6Bve3dcv10uZJ0FCnlj+12LQaSTiH9F7spXS6lo7wdWqf4jMDMrHC+R2BmVjgHgZlZ4RwEZmaFcxCYmRXOQWBmVrj/D2OVCVpn6aqNAAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a id='conclusions'></a></p>
<h2 id="Conclusions">Conclusions<a class="anchor-link" href="#Conclusions">&#182;</a></h2><p>Congratulations on completing the project! This is only a sampling of the data analysis process: from generating questions, wrangling the data, and to exploring the data. Normally, at this point in the data analysis process, you might want to draw conclusions about the data by performing a statistical test or fitting the data to a model for making predictions. There are also a lot of potential analyses that could be performed on the data which are not possible with only the data provided. For example, detailed location data has not been investigated. Where are the most commonly used docks? What are the most common routes? As another example, weather has potential to have a large impact on daily ridership. How much is ridership impacted when there is rain or snow? Are subscribers or customers affected more by changes in weather?</p>
<p><strong>Question 7</strong>: Putting the bike share data aside, think of a topic or field of interest where you would like to be able to apply the techniques of data science. What would you like to be able to learn from your chosen subject?</p>
<p><strong>Answer</strong>: Social Networking Website</p>

<pre><code>        1. How many users are currently online?
        2. Which country spends more time online?
        3. Which Gender is more active ?
        4. Which Age group is posting more updates ?


</code></pre>
<blockquote><p><strong>Tip</strong>: If we want to share the results of our analysis with others, we aren't limited to giving them a copy of the jupyter Notebook (.ipynb) file. We can also export the Notebook output in a form that can be opened even for those without Python installed. From the <strong>File</strong> menu in the upper left, go to the <strong>Download as</strong> submenu. You can then choose a different format that can be viewed more generally, such as HTML (.html) or
PDF (.pdf). You may need additional packages or software to perform these exports.</p>
<p>If you are working on this project via the Project Notebook page in the classroom, you can also submit this project directly from the workspace. <strong>Before you do that</strong>, you should save an HTML copy of the completed project to the workspace by running the code cell below. If it worked correctly, the output code should be a 0, and if you click on the jupyter icon in the upper left, you should see your .html document in the workspace directory. Alternatively, you can download the .html copy of your report following the steps in the previous paragraph, then <em>upload</em> the report to the directory (by clicking the jupyter icon).</p>
<p>Either way, once you've gotten the .html report in your workspace, you can complete your submission by clicking on the "Submit Project" button to the lower-right hand side of the workspace.</p>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[64]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">subprocess</span> <span class="k">import</span> <span class="n">call</span>
<span class="n">call</span><span class="p">([</span><span class="s1">&#39;python&#39;</span><span class="p">,</span> <span class="s1">&#39;-m&#39;</span><span class="p">,</span> <span class="s1">&#39;nbconvert&#39;</span><span class="p">,</span> <span class="s1">&#39;Bike_Share_Analysis.ipynb&#39;</span><span class="p">])</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

<div class="prompt output_prompt">Out[64]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0</pre>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
