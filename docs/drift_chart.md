# Drift Detection Results

% Change from Reference to Current Period

<div style="max-width:800px;margin:0 auto">
<canvas id="driftChart"></canvas>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<script>
const ctx = document.getElementById('driftChart').getContext('2d');
new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Requests', 'Errors', 'Latency (ms)'],
        datasets: [{
            label: '% Change from Reference',
            data: [28.22, 173.91, 47.85],
            backgroundColor: ['#4e79a7', '#e15759', '#f28e2b'],
            borderRadius: 6,
        }]
    },
    options: {
        plugins: { legend: { display: false } },
        scales: {
            y: { ticks: { callback: (v) => `${v}%` } }
        }
    }
});
</script>
