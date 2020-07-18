<script>
import { Bar } from 'vue-chartjs'

export default {
  name: "Bar",
  extends: Bar,
  data: () => ({
    chartdata: {
      labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun'],
       datasets: [{
            label: 'Montly Spendings',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235,1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
  }),

  mounted () {
    if(window) {
      this.renderChart(this.chartdata, this.options)
    }
  }
}
</script>
