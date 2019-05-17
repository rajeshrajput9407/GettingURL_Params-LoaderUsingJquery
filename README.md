# GettingURL_Params-LoaderUsingJquery
Get the parameter of Get URL and Loader of Screen using Jquery

# GEt url parameter from the URL

 ```$.urlParam = function (name) {
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
        ```
        
