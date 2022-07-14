<script lang="ts">
  import "carbon-components-svelte/css/all.css";
  import { Dropdown, Modal, TextInput } from "carbon-components-svelte";
</script>

<Modal
  open={true}
  modalHeading={`A11y issue`}
  primaryButtonText="OK"
  secondaryButtonText="Cancel"
  hasScrollingContent={true}
  on:open
  on:close
>
  <h3>Try to hit TAB and iterate across inputs</h3>
  <h3>Then same with Shift-TAB</h3>
  <div>
    <a href="/">Dropdown first</a>
    <br />
    <a href="/reverse">Inputs first</a>
  </div>

  <div class="content">
    <Dropdown
      titleText="Select source"
      selectedId={"0"}
      items={[
        { id: "0", text: "First item" },
        { id: "1", text: "Second item" },
      ]}
    />
    <TextInput placeholder="text" name="text" labelText="Login" />
    <TextInput placeholder="password" type="password" labelText="Password" />
  </div>
</Modal>

<style>
  .content {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-top: 1rem;
  }
</style>
