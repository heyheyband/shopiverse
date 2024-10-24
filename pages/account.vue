<template>
    <div>
        

<div class="relative overflow-x-auto">
    <br><br>
    <table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
        <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
            <tr>
                <th scope="col" class="px-6 py-3">
                    Avatar
                </th>
                <th scope="col" class="px-6 py-3">
                    Name
                </th>
                <th scope="col" class="px-6 py-3">
                    Email
                </th>
                <th scope="col" class="px-6 py-3">
                    Username
                </th>
                <th scope="col" class="px-6 py-3">
                    Id
                </th>
            </tr>
        </thead>
        <tbody v-if="user">
            <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
                <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                    <img :src="user.user_metadata.avatar_url" />
                </th>
                <td class="px-6 py-4">
                    {{ user.user_metadata.name }}
                </td>
                <td class="px-6 py-4">
                    {{user.email}}
                </td>
                <td class="px-6 py-4">
                    {{ user.user_metadata.user_name }}
                </td>
                <td class="px-6 py-4">
                    {{ user.id }}
                </td>
            </tr>
            
        </tbody>
    </table>
</div>

    </div>
</template>

<script setup>

    const supabase = useSupabaseClient()
    const user = useSupabaseUser()



</script>

