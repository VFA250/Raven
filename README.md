# Raven
![RavenTool](https://github.com/user-attachments/assets/84c632e0-46c5-4f74-99a9-01be63d9ef5e)
Raven is a powerful and customizable web crawler written in Go. It allows you to extract internal and external links from a given website with options for concurrent crawling, depth customization, and maximum URL limits.
## Features
- Concurrent crawling to maximize efficiency.
- Customizable depth and maximum URL limits to tailor the crawling process to your needs.
- Extraction of both internal and external links for comprehensive analysis.
- Colorful logging for easy debugging and tracking of crawling progress.
- Error handling for fetching URLs to ensure robustness.

## Installation
To install Raven, you have three options,

⚠️ **Ensure you have Go installed on your system. If not, you can download it from the official Go website.** ⚠️

1. [Compiled Version](https://github.com/VFA250/Raven/releases)

2. Clone the Raven repository
```sh
git clone https://github.com/VFA250/Raven.git
```

- Navigate to the project directory
```sh
cd raven
```

- Build the project
```sh
go build
```

3. To install Raven, use go get
```sh
go get github.com/VFA250/raven
```

## Usage
```sh
chmod +x raven
```

```sh
./raven [options] <startURL>
```

⚠️ startURL: The starting URL from which the crawling process begins. ⚠️

## Options
1. -maxURLs <value>: Maximum number of URLs to crawl (default: 100)
2. -maxDepth <value>: Maximum depth of crawling (default: 3)
3. -concurrency <value>: Number of concurrent requests (default: 10)

## Example

```sh
./raven -maxURLs 500 -maxDepth 5 -concurrency 20 https://target.com
```

This command will crawl the website https://target.com with a maximum of 500 URLs, a maximum depth of 5, and 20 concurrent requests.

## Dependencies

1. Raven depends on the following external packages:
golang.org/x/net/html : Used for HTML parsing.

2. You can install these dependencies using the following command
```sh
go mod tidy
```

## License
This project is licensed under the MIT License. See the LICENSE file for details.
