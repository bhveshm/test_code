# test_code
<style>
    .k-pager-wrap .k-dropdown {
        display: inline-block;
        vertical-align: middle;
    }

    .k-pager-wrap #pagerSlider {
        display: inline-block;
        vertical-align: middle;
    }
</style>

<script>
    $(document).ready(function () {
        // Find the pager and insert the switch
        var pagerElement = $("#kendoGrid .k-grid-pager");
        var switchHtml = '<div id="pagerSlider" class="k-switch k-switch-off"><span class="k-switch-handle"></span></div>';
        pagerElement.find(".k-pager-sizes").after(switchHtml);

        // Initialize the Kendo Switch
        $("#pagerSlider").kendoSwitch({
            change: function (e) {
                // Perform any additional actions based on the state
                var switchState = e.sender.value();
                console.log("Switch state:", switchState);
            }
        });
    });
</script>
