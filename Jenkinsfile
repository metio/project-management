node {
    stage("configuration") {
        jobDsl targets: ['configFiles.groovy'].join('\n')
    }

    stage("sebhoss") {
        jobDsl scriptText: 'folder("sebhoss")'

        jobDsl targets: ['sebhoss/verify.groovy', 'sebhoss/views.groovy'].join('\n'),
               removedJobAction: 'DELETE',
               removedViewAction: 'DELETE'
    }

}
