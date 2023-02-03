<script lang="ts">
import { createEventDispatcher } from 'svelte';

const weapon = {
  name: '',
  level: '1',
};

const dispatch = createEventDispatcher();

type ChangeEvent = Event & { currentTarget: EventTarget & HTMLSelectElement };
const handleChanges = (nameEvent?: ChangeEvent, levelEvent?: ChangeEvent) => {
  if (nameEvent) {
    weapon.name = nameEvent.currentTarget?.value;
  }

  if (levelEvent) {
    weapon.level = levelEvent.currentTarget?.value;
  }

  dispatch('change', weapon);
};

</script>

<select on:change={(e) => handleChanges(e)}>
  <option>The black Sword</option>
</select>

<select on:change={(e) => handleChanges(undefined, e)}>
  <option>80</option>
  <option>80 Ascend</option>
</select>