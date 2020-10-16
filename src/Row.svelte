<script>

    export let tool;
    export let state;
    export let link;

    const setBadge = (state) => {
        let badgeStyle = "new badge";
        switch (state) {
            case "Assess":
                badgeStyle = `${badgeStyle} yellow`;
                break;
            case "Trial":
                badgeStyle = `${badgeStyle} blue`;
                break;
            case "Hold":
                badgeStyle = `${badgeStyle} red`;
                break;
            case "Adopt":
                badgeStyle = `${badgeStyle} green`;
                break;
            default:
                badgeStyle = `${badgeStyle} grey`;
                break;
        }
        return badgeStyle;
    }
</script>

<tr>
    <td>{tool}</td>
    <td><span class={setBadge(state)} data-badge-caption="{state}"></span></td>
    <td><a href="{link}" target="_blank">{link}</a></td>
</tr>

