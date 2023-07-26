<script setup>
import { Navbar, NavbarLogo, NavbarCollapse, NavbarLink } from 'flowbite-vue'
</script>
<template>
    <Navbar solid>
      <template #logo>
        <NavbarLogo link="https://www.google.com/" alt="Flowbite logo" image-url="https://marketplace.canva.com/EAFLwMyCpjY/1/0/800w/canva-ungu-dan-merah-minimalis-logo-toko-baju-anak-RRmvaV4T7DU.jpg">
          Flowbite
        </NavbarLogo>
      </template>
      <template #default="{isShowMenu}">
        <NavbarCollapse :isShowMenu="isShowMenu">
          <NavbarLink is-active>Home</NavbarLink>
          <NavbarLink>Services</NavbarLink>
          <NavbarLink>Pricing</NavbarLink>
          <NavbarLink>Contact</NavbarLink>
        </NavbarCollapse>
      </template>
    </Navbar>
</template>