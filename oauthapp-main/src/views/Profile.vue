<template>
    <div>
        <div>
            <img :src="$auth.user.picture"/>
            <h2>{{ $auth.user.name }}</h2>
            <h5>{{ $auth.user.email }}</h5>
        </div>
        <div>
            <pre>{{ JSON.stringify($auth.user, null, 2) }}</pre>
        </div>
    </div>
</template>