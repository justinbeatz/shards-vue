<template>
    <div>
        <d-button @click="handleClick">Click me!</d-button>
        <d-link href="#">Some link</d-link>
        <div>
            <d-dropdown text="Dropdown">
                <d-dropdown-item @click="handleClick">
                    Click me!
                </d-dropdown-item>
            </d-dropdown>
        </div>
    </div>
</template>

<script>
/**
 * 🙌 Awesome, so you'd like to contribute!
 *
 * You can use this file to experiment with Shards Vue, add a new
 * feature or maybe fix a bug. All you need to do is work inside
 * this file! That's it!
 *
 * Check out the comments below to understand what's going on!
 */

// First we're importing Vue
// eslint-disable-next-line
import Vue from 'vue'

// We're also importing Bootstrap's and Shards' styles
import 'bootstrap/dist/css/bootstrap.css'
import 'shards-ui/dist/css/shards.css'

// We're importing one of Shards Vue's components and registering it as a Vue Plugin
// eslint-disable-next-line
import { Button } from '../src/components'

// Uncomment this line in case you'd like to use the component as a plugin
// Vue.use(Button)

// ALTERNATIVE: Import the component directly.
import dButton from '../src/components/button/Button';
import dLink from '../src/components/link/Link.vue';
import dDropdown from '../src/components/dropdown/Dropdown.vue';
import dDropdownItem from '../src/components/dropdown/DropdownItem.vue';

// We define our custom component's logic.
export default {
    components: {
        dButton,
        dDropdown,
        dDropdownItem,
        dLink
    },
    methods: {
        handleClick() {
            alert('You just clicked me!')
        }
    }
}
</script>
