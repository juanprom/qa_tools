<script>
    export let tool;
    export let state;
    export let link;

    const setBadge = (state) => {
        const badge = "new badge";
        let badgeStyle;
        switch (state) {
            case "Assess":
                badgeStyle = `${badge} yellow`;
                break;
            case "Trial":
                badgeStyle = `${badge} blue`;
                break;
            case "Hold":
                badgeStyle = `${badge} red`;
                break;
            case "Adopt":
                badgeStyle = `${badge} green`;
                break;
            default:
                badgeStyle = `${badge} grey`;
                break;
        }
        return badgeStyle;
    }
</script>

<tr>
    <td>
        <button class="waves-effect waves-light btn">
            {tool}
        </button>
    </td>
    <td><span class={setBadge(state)}>{state}</span></td>
    <td><a href="{link}" target="_blank">{link}</a></td>
</tr>