# GettingURL_Params-LoaderUsingJquery
Get the parameter of Get URL and Loader of Screen using Jquery

# GEt url parameter from the URL

 $.urlParam = function (name) {
            var results = new RegExp('[\?&]' + name + '=([^&#]*)').exec(window.location.href);
            if (results == null) {
                return null;
            }
            return decodeURI(results[1]) || 0;
        }

        $("#btnSave").on("click", function () {
            debugger;
            var uri = this.baseURI;
            var ContId = $("#ContId").text();
            var ContType = $("#ContType").text();
            var userName = $.urlParam('username');
            var clientId = $.urlParam('clientid');
            var password = $.urlParam('password');
        })
	
#Ajax Loader using Jquery
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width" />
    <title>ImageLoadingDemo</title>
    <style>
        .center-div {
            width: 300px;
            height: 300px;
            position: absolute;
            left: 50%;
            top: 50%;
            margin-left: -150px;
            margin-top: -150px;
        }

        .spinner {
            position: fixed;
            z-index: 999;
            height: 100%;
            width: 100%;
            top: 0;
            left: 0;
            background-color: Black;
            filter: alpha(opacity=60);
            opacity: 0.6;
            -moz-opacity: 0.8;
        }
        <!-- .loader { -->
            <!-- margin: auto; -->
            <!-- border: 16px solid #f3f3f3; -->
            <!-- border-radius: 50%; -->
            <!-- border-top: 16px solid #15a0ec; -->
            <!-- border-bottom: 16px solid #15a0ec; -->
            <!-- width: 120px; -->
            <!-- height: 120px; -->
            <!-- -webkit-animation: spin 2s linear infinite; -->
            <!-- animation: spin 2s linear infinite; -->
        <!-- } -->

        .inner-div {
            background-color: white;
            border-radius: 15px;
            margin: auto;
            padding: 16%;
            width: 45px;
        }

        @@-webkit-keyframes spin {
            0% {
                -webkit-transform: rotate(0deg);
            }

            100% {
                -webkit-transform: rotate(360deg);
            }
        }

        @@keyframes spin {
            0% {
                transform: rotate(0deg);
            }

            100% {
                transform: rotate(360deg);
            }
        }
    </style>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
    <script>
        $(document).ready(function () {
           
                $('.spinner').css('display', 'block');
             
        });
    </script>
	<script type="text/javascript">
        window.onload = function () {
            setTimeout(function () {
<!--                 document.body.removeChild(modal); -->
<!--                 loading.style.display = "none"; -->
$('.spinner').css('display', 'none');
            }, 387000);
        };
    </script>
</head>
<body>
    <div> 
        <input type="button" id="btnSubmit" value="Submit" />

        <div class="spinner" style="display:none">
            <div class="center-div">
                <div class="inner-div">
                    <div class="loader">
					 <img src="https://www.aspsnippets.com/demos/loader.gif" alt="" />
					</div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
