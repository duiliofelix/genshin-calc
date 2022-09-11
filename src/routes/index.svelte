<script lang="ts">
import InputPanel from "../components/InputPanel.svelte";
import CharPicker from "../components/CharPicker.svelte";
</script>

<CharPicker />
<div class="content">
  <InputPanel />
  <div>
    <div>
      <table>
        <thead>
          <tr>
            <th>Stat</th>
            <th>Base</th>
            <th>Mod</th>
            <th>Total</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>hp</td>
            <td>1</td>
            <td>1</td>
            <td>2</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div>
      Autos
      Elemental
      Burst
      Reações
    </div>
  </div>
</div>

<style>
.content {
  display: flex;
  padding: 10px 0;
}
</style>