<template>
  <div class="d-flex flex-column">
    <Navbar />

    <Splitpanes @resized="handleResized" class="default-theme">
      <Pane :size="sidebarSize" :data-size="sidebarSize" :class="{ 'is-closed': !sidebarOpen }">
        <Sidebar />
      </Pane>

      <Pane :size="pageSize" :data-size="pageSize" :class="{ 'is-wide': !sidebarOpen }" min-size="50">
        <div class="page-wrapper">
          <button @click="toggleSidebar" :class="['btn btn-icon splitpanes__toggler', { 'is-closed': !sidebarOpen }]">
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-chevron-left" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="15 6 9 12 15 18"></polyline></svg>
          </button>

          <div class="container-fluid">
            <div class="page-header">
              <div class="row align-items-center">
                <div class="col">
                  <div class="page-pretitle">
                    Overview
                  </div>

                  <h2 class="page-title">QBricks Splitpanes</h2>

                  <slot />
                </div>
              </div>
            </div>

            <div class="page-body">
              <div class="container-fluid">
                <div class="row row-deck row-cards">
                  <!-- Sample Stats  -->

                  <div class="col-3">
                    <div class="card">
                      <div class="card-body p-2 text-center">
                        <div class="text-end text-green">
                          <span class="text-green d-inline-flex align-items-center lh-1">
                            6%
                            <svg xmlns="http://www.w3.org/2000/svg" class="icon ms-1" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="3 17 9 11 13 15 21 7"></polyline><polyline points="14 7 21 7 21 14"></polyline></svg>
                          </span>
                        </div>
                        <div class="h1 m-0">43</div>
                        <div class="text-muted mb-3">New Tickets</div>
                      </div>
                    </div>
                  </div>

                  <div class="col-3">
                    <div class="card">
                      <div class="card-body p-2 text-center">
                        <div class="text-end text-green">
                          <span class="text-green d-inline-flex align-items-center lh-1">
                            23%
                            <svg xmlns="http://www.w3.org/2000/svg" class="icon ms-1" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="3 17 9 11 13 15 21 7"></polyline><polyline points="14 7 21 7 21 14"></polyline></svg>
                          </span>
                        </div>
                        <div class="h1 m-0">$23,432.59</div>
                        <div class="text-muted mb-3">Income</div>
                      </div>
                    </div>
                  </div>

                  <div class="col-3">
                    <div class="card">
                      <div class="card-body p-2 text-center">
                        <div class="text-end text-red">
                          <span class="text-red d-inline-flex align-items-center lh-1">
                            -2%
                            <svg xmlns="http://www.w3.org/2000/svg" class="icon ms-1" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="3 7 9 13 13 9 21 17"></polyline><polyline points="21 10 21 17 14 17"></polyline></svg>
                          </span>
                        </div>
                        <div class="h1 m-0">95</div>
                        <div class="text-muted mb-3">Daily Earnings</div>
                      </div>
                    </div>
                  </div>

                  <div class="col-3">
                    <div class="card">
                      <div class="card-body p-2 text-center">
                        <div class="text-end text-green">
                          <span class="text-green d-inline-flex align-items-center lh-1">
                            9%
                            <svg xmlns="http://www.w3.org/2000/svg" class="icon ms-1" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="3 17 9 11 13 15 21 7"></polyline><polyline points="14 7 21 7 21 14"></polyline></svg>
                          </span>
                        </div>
                        <div class="h1 m-0">7</div>
                        <div class="text-muted mb-3">New Replies</div>
                      </div>
                    </div>
                  </div>

                  <!-- Sample Table -->
                  <div class="col-12">
                    <div class="card">
                      <div class="card-header">
                        <h3 class="card-title">Social Media Traffic</h3>
                      </div>
                      <table class="table card-table table-vcenter">
                        <thead>
                          <tr>
                            <th>Network</th>
                            <th colspan="2">Visitors</th>
                          </tr>
                        </thead>
                        <tbody>
                          <tr>
                            <td>Instagram</td>
                            <td>3,550</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 71.0%"></div>
                              </div>
                            </td>
                          </tr>
                          <tr>
                            <td>Twitter</td>
                            <td>1,798</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 35.96%"></div>
                              </div>
                            </td>
                          </tr>
                          <tr>
                            <td>Facebook</td>
                            <td>1,245</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 24.9%"></div>
                              </div>
                            </td>
                          </tr>
                          <tr>
                            <td>TikTok</td>
                            <td>986</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 19.72%"></div>
                              </div>
                            </td>
                          </tr>
                          <tr>
                            <td>Pinterest</td>
                            <td>854</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 17.08%"></div>
                              </div>
                            </td>
                          </tr>
                          <tr>
                            <td>VK</td>
                            <td>650</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 13.0%"></div>
                              </div>
                            </td>
                          </tr>
                          <tr>
                            <td>Pinterest</td>
                            <td>420</td>
                            <td class="w-50">
                              <div class="progress progress-xs">
                                <div class="progress-bar bg-primary" style="width: 8.4%"></div>
                              </div>
                            </td>
                          </tr>
                        </tbody>
                      </table>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <footer class="footer footer-transparent text-center">
            <p>
              Made with
              <span class="text-vue">♥</span>
              by
              <a href="https://github.com/schodevio" target="_blank" rel="noopener" class="author">schodevio</a>
            </p>
          </footer>
        </div>
      </Pane>
    </Splitpanes>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import { Splitpanes, Pane } from 'splitpanes'

import Navbar from '@/components/Navbar.vue'
import Sidebar from '@/components/Sidebar.vue'

import { PaneType, SizeType } from '@/types/PaneTypes'

export default defineComponent({
  components: { Splitpanes, Pane, Navbar, Sidebar },
  setup() {
    // Sizes
    const sidebarSize = ref<SizeType>(localStorage.getItem('sidebarSize') || 20)
    const pageSize = ref<SizeType>(localStorage.getItem('pageSize') || 80)

    const handleResized = ([sidebar, page]: PaneType[]): void => {
      sidebarSize.value = sidebar.size
      pageSize.value = page.size

      localStorage.setItem('sidebarSize', `${sidebar.size}`)
      localStorage.setItem('pageSize', `${page.size}`)
    }

    // Open / Close

    const sidebarOpen = ref<boolean>(
      ['true', null].includes(localStorage.getItem('sidebarOpen'))
    )

    const toggleSidebar = (): void => {
      const newValue = !sidebarOpen.value

      sidebarOpen.value = newValue
      localStorage.setItem('sidebarOpen', `${newValue}`)
    }

    return {
      sidebarSize,
      pageSize,
      handleResized,

      sidebarOpen,
      toggleSidebar
    }
  }
})
</script>
