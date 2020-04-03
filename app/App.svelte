<page>
    <actionBar title="My App" icon="">
    </actionBar>
    <stackLayout class="p-20">
    <label text="Top the button" class="h1 text-center"/>
    <button text="TAP" on:tap="{ onTap }" class="-primary -active"/>
    <label text="{ message }" class="h2 text-center" textWrap="true"/>
    <label text="Hello" />
    <datePicker />
    <Color />
    </stackLayout>

</page>

<script>
    import Color from './Color.svelte';
    let counter = 42;
    let message;
    $: message = (counter <= 0)
            ? "Hoorraaay! You unlocked the Svelte-Native clicker achievement!"
            : `${counter} taps left`

    const onTap = () => counter--;        

</script>

