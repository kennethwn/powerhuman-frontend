<template>
  <div class="app">
    <ol>
      <li v-for="role in data.data" :key="role.id">
        {{ role.name }}
      </li>
    </ol>
  </div>
</template>

<script>
  export default {
    el: '#app',
    name: 'CompanyPage',
    data() {
      return {
        meta: {
          code: 200,
          status: "success",
          message: "Roles is exists"
        },
        data: {
          current_page: 1,
          data: [
            {
              id: 12,
              name: "Developer",
              company_id: 49,
              deleted_at: null,
              created_at: "2023-08-24T17:46:12.000000Z",
              updated_at: "2023-08-24T17:46:12.000000Z",
              responsibilities: [
                {
                  id: 201,
                  name: "Fullstack developer for website",
                  role_id: 12,
                  deleted_at: null,
                  created_at: "2023-08-25T07:03:39.000000Z",
                  updated_at: "2023-08-25T07:03:39.000000Z"
                },
                {
                  id: 203,
                  name: "Frontend engineer for website",
                  role_id: 12,
                  deleted_at: null,
                  created_at: "2023-08-25T07:26:23.000000Z",
                  updated_at: "2023-08-25T07:26:23.000000Z"
                }
              ]
            },
            {
              id: 13,
              name: "Database Developer",
              company_id: 49,
              deleted_at: null,
              created_at: "2023-08-28T13:46:11.000000Z",
              updated_at: "2023-08-28T13:46:11.000000Z",
              responsibilities: []
              }
          ],
            first_page_url: "http://127.0.0.1:8000/api/role?page=1",
            from: 1,
            last_page: 1,
            last_page_url: "http://127.0.0.1:8000/api/role?page=1",
            links: [
            {
              url: null,
              label: "&laquo; Previous",
              active: false
            },
            {
              url: "http://127.0.0.1:8000/api/role?page=1",
              label: "1",
              active: true
            },
            {
              url: null,
              label: "Next &raquo;",
              active: false
            }
          ],
            next_page_url: null,
            path: "http://127.0.0.1:8000/api/role",
            per_page: 10,
            prev_page_url: null,
            to: 2,
            total: 2
        }
      }
    },
  }
</script>
