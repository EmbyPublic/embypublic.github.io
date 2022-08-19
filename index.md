<h3>URL 重定向中</h3>

<script>
// https://embypublic.github.io/index.html?url-schema=[经过 encodeURIComponent 编码的 URL Schema]

var url_schema = decodeURIComponent(getQueryVariable('url-schema'));

location.href = url_schema;

function getQueryVariable(variable)
{
    var query = window.location.search.substring(1);
    var vars = query.split("&");
    for (var i=0;i<vars.length;i++) {
        var pair = vars[i].split("=");
        if(pair[0] == variable){return pair[1];}
    }
    return(false);
}
</script>
