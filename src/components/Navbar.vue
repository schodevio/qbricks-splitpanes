<template>
  <header class="navbar navbar-expand-md navbar-dark">
    <div class="container-fluid">
      <h1 class="navbar-brand navbar-brand-autodark pe-3">
        <a href="#">Company Ltd</a>
      </h1>

      <div id="navbar-menu" class="navbar-collapse collapse">
        <div class="d-flex flex-row flex-fill align-items-stretch">
          <ul class="navbar-nav flex-grow-1">
            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="nav-link-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="5 12 3 12 12 3 21 12 19 12"></polyline><path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7"></path><path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6"></path></svg>
                </span>

                <span class="nav-link-title">
                  Home
                </span>
              </a>
            </li>

            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="nav-link-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><circle cx="9" cy="7" r="4"></circle><path d="M3 21v-2a4 4 0 0 1 4 -4h4a4 4 0 0 1 4 4v2"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path><path d="M21 21v-2a4 4 0 0 0 -3 -3.85"></path></svg>
                </span>

                <span class="nav-link-title">
                  Customers
                </span>
              </a>
            </li>

            <li class="nav-item dropdown">
              <a class="nav-link" href="#">
                <span class="nav-link-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><line x1="18" y1="6" x2="18" y2="6.01"></line><path d="M18 13l-3.5 -5a4 4 0 1 1 7 0l-3.5 5"></path><polyline points="10.5 4.75 9 4 3 7 3 20 9 17 15 20 21 17 21 15"></polyline><line x1="9" y1="4" x2="9" y2="17"></line><line x1="15" y1="15" x2="15" y2="20"></line></svg>
                </span>

                <span class="nav-link-title">
                  Locations
                </span>
              </a>
            </li>

            <li class="nav-item dropdown">
              <a class="nav-link" href="#">
                <span class="nav-link-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><path d="M9 4h3l2 2h5a2 2 0 0 1 2 2v7a2 2 0 0 1 -2 2h-10a2 2 0 0 1 -2 -2v-9a2 2 0 0 1 2 -2"></path><path d="M17 17v2a2 2 0 0 1 -2 2h-10a2 2 0 0 1 -2 -2v-9a2 2 0 0 1 2 -2h2"></path></svg>
                </span>

                <span class="nav-link-title">
                  Documents
                </span>
              </a>
            </li>
          </ul>

          <div class="m-2">
            <form action="." method="get">
              <div class="input-icon">
                <span class="input-icon-addon">
                  <svg xmlns="http://www.w3.org/2000/svg" class="icon" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><circle cx="10" cy="10" r="7"></circle><line x1="21" y1="21" x2="15" y2="15"></line></svg>
                </span>

                <input type="text" class="form-control" placeholder="Search…" aria-label="Search in website">
              </div>
            </form>
          </div>

          <div class="navbar-nav d-flex align-items-center">
            <span class="avatar avatar-sm text-white bg-blue">JD</span>
            <div class="d-block ps-2">
              <div class="text-white">John Doe</div>
              <div class="small text-muted">Admin User</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Navbar'
})
</script>
