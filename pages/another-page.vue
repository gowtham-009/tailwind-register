<template>
    <div class="w-full flex flex-col justify-center items-center mt-5">
        <H1 class="text-red-500">Form Details</H1>
        <div class="grid grid-cols-2 md:grid-cols-1 gap-5 mt-5">
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">User name:{{$route.query.username}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Email:{{$route.query.email}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Phone Number:{{$route.query.mobile}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Date of birth:{{$route.query.dob}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Gender:{{$route.query.gender}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Address:{{$route.query.address}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Country:{{$route.query.country}}</div>
            <div class="text-white text-lg border-solid border-2 border-red-500 p-3">Postal:{{$route.query.postal}}</div>
        </div>
    </div>
</template>
<style>
h1{
    font-size: 2rem;
}
</style>