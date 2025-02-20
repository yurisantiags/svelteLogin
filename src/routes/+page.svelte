<script lang="ts">
    
    interface BasketballStats {
    points: number;
    rebounds: number;
    assists: number;
    steals: number;
    }


    let stats: BasketballStats = {
    points: 120,
    rebounds: 45,
    assists: 32,
    steals: 15
    };
</script>

<style>

    .background-video {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: -1;
    }

    .dashboard {
    position: relative;
    z-index: 1;
    color: white;
    padding: 20px;
    font-family: 'Arial', sans-serif;
    }

    .stat-card {
    background: rgba(0, 0, 0, 0.6);
    padding: 20px;
    border-radius: 8px;
    margin: 10px 0;
    }
</style>

<main class="flex items-center justify-center h-screen bg-black">

    <video autoplay loop muted class="background-video">
    <source src="/basketball.mp4" type="video/mp4" />
    Your browser does not support the video tag.
    </video>


    <div class="dashboard text-center">
        <h1 class="text-4xl font-bold mb-6">Basketball Stats</h1>
    <div class="stat-card">
        <h2 class="text-2xl mb-2">Points</h2>
        <p class="text-3xl">{stats.points}</p>
    </div>
    
    <div class="stat-card">
        <h2 class="text-2xl mb-2">Rebounds</h2>
        <p class="text-3xl">{stats.rebounds}</p>
    </div>

    <div class="stat-card">
        <h2 class="text-2xl mb-2">Assists</h2>
        <p class="text-3xl">{stats.assists}</p>
    </div>

    <div class="stat-card">
        <h2 class="text-2xl mb-2">Steals</h2>
        <p class="text-3xl">{stats.steals}</p>
    </div>
    </div>
</main>
