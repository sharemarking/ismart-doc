# ismart-doc
### An API documentation generator base of [modoc](https://github.com/mhbseal/modoc)

#### Install and Run

npm

    npm install ismart-doc -g
    
    smartdoc --config <configPath>

github
    
    git clone https://github.com/hnzxb/ismart-doc
    cd ismart-doc && npm install
    
    node index.js --config <configPath>

#### Example
source contains mojs example,so wen can Enter 'exmpale' directory after install(npm or github)

npm

    ismart-doc

github

    node ../index

#### Config
    /ismart.config.js
    module.exports = {
        doc: {
            name         : "ismart-path",
            title        : "Path扩展-ismart",
            version      : "0.1.0",
            repositoryUrl: "https://github.com/hnzxb/ismart-path",
            introduction : '描述',
            paths        : {
                input : "./src",
                output: "./readme"
            },
            source       : '',
            skip         : []
        }
    }
    
#### Comment Example
  
general document comment

    /**
     * description
     *
     * @param {string} 1
     * @param {object} 2
     *   - a {number} 3
     *   - b {string} 4
     * @param {function} 5
     *   - param {number} 6
     *   - param {function} 7
     *     - param 8
     * @return {object} 9
     *   - c {string} 10
     *   - d {number} 11
     */

after add generator
    
    /**
     * description
     *
     * @param {string} 1
     * @param {object} 2
     *   - a {number} 3
     *   - b {string} 4
     * @param {function} 5
     *   - param {number} 6
     *   - param {function} 7
     *     - param 8
     * @return {object} 9
     *   - c {string} 10
     *   - d {number} 11
     * 
     * @name file name or method name or property name(required)
     * @example
     * var str = 'doc';
     * num.toUpperCase();
     * ...
     * @more
     * this is more information,
     * let go.
     * ...
     */
